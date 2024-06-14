A single-page, one-column resume for software developers. It uses the base latex templates and fonts to provide ease of use and installation when trying to update the resume. The different sections are clearly documented and custom commands are used to provide consistent formatting. The three main sections in the resume are education, experience, and projects.

### Motivation

I created this template as managing a resume on Google Docs was hard and changing any formatting was too difficult since it had to be applied in multiple places.

Most currently available templates either focus on two columns, or are multiple pages long that didn't work well for career fairs or online applications.

### Quick start

Get started quickly using [Overleaf](https://www.overleaf.com/latex/templates/software-engineer-resume/gqxmqsvsbdjf) template.

### Build using Docker

```sh
docker build -t latex .
docker run --rm -i -v "$PWD":/data latex pdflatex vu_xuan_quy.tex
or
docker run --rm -i -v "D:\cv_clone\resume:/data" latex pdflatex vu_xuan_quy.tex
```

### Preview

![Resume Screenshot](/resume_preview1.png)
![Resume Screenshot](/resume_preview2.png)

### License

Format is MIT but all the data is owned by Sourabh Bajaj.
