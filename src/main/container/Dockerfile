FROM squidfunk/mkdocs-material:7.2.0
RUN apk --update --upgrade --no-cache add gcc build-base musl-dev jpeg-dev libzmq zlib-dev libffi-dev cairo-dev pango-dev gdk-pixbuf-dev zeromq-dev python3-dev graphviz
RUN pip install --no-cache-dir pyzmq graphviz jupytext openpyxl diagrams mike pandas notebook mkpdfs-mkdocs mkdocs-with-pdf mkdocs-table-reader-plugin mkdocs-diagrams mkdocs-jupyter
#RUN pip install --no-cache-dir git+https://github.com/jwaschkau/mkpdfs-mkdocs-plugin.git#egg=mkpdfs-mkdocs-plugin --upgrade
#RUN apk del --no-cache build-base musl-dev python3-dev zeromq-dev jpeg-dev zlib-dev libffi-dev cairo-dev pango-dev gdk-pixbuf-dev
# Additional font
COPY /maven /usr/share/fonts/Additional
RUN apk --update --upgrade --no-cache add fontconfig ttf-freefont font-noto terminus-font \
    && fc-cache -f \
    && fc-list | sort