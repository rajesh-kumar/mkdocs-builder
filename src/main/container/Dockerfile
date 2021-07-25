FROM squidfunk/mkdocs-material:7.1.9
RUN apk --update --upgrade --no-cache add gcc build-base musl-dev jpeg-dev zlib-dev libffi-dev cairo-dev pango-dev gdk-pixbuf-dev graphviz 
RUN pip install --no-cache-dir mike mkpdfs-mkdocs mkdocs-with-pdf mkdocs-table-reader-plugin openpyxl diagrams jupytext mkdocs-diagrams pandas notebook mkdocs-jupyter
#RUN pip install --no-cache-dir git+https://github.com/jwaschkau/mkpdfs-mkdocs-plugin.git#egg=mkpdfs-mkdocs-plugin --upgrade
# Additional font
COPY /maven /usr/share/fonts/Additional
RUN apk --update --upgrade --no-cache add fontconfig ttf-freefont font-noto terminus-font \
    && fc-cache -f \
    && fc-list | sort