---
name: latex-to-pdf
description: Convert LaTeX (.tex) to PDF using lightweight Docker image
user_invocable: true
---

## Dockerfile (Dockerfile.minimal)

```dockerfile
FROM alpine:3.19

RUN apk add --no-cache texlive texmf-dist-latexextra \
    && rm -rf /var/cache/apk/*

WORKDIR /data
VOLUME ["/data"]
```

## Build image (chỉ cần chạy 1 lần)

```bash
docker build -f Dockerfile.minimal -t latex-minimal .
```

## Convert .tex to .pdf

```bash
docker run --rm -v "/Users/quyvx/Documents/ca-nhan/resume":/data -w /data latex-minimal pdflatex vu_xuan_quy.tex
```

## Notes
- Image `latex-minimal`: ~1.22GB (Alpine + texlive + latexextra)
- Không cần `texmf-dist-fontsextra` (tiết kiệm ~2.5GB)
- Nếu chưa có image, build trước rồi mới convert
