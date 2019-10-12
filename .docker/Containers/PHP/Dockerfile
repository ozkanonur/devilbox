ARG VERSION
FROM devilbox/php-fpm:${VERSION}-work-0.89

ARG NODE_VERSION

RUN apt-get update && apt-get install -y \
    curl

RUN sudo apt-get update && \
    sudo apt-get install -y xvfb libfontconfig wkhtmltopdf && \
    sudo apt-get install -y ghostscript

RUN curl --silent -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.0/install.sh | bash && \
    . /root/.nvm/nvm.sh && \
    nvm install ${NODE_VERSION}