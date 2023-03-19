FROM python:3.10-slim

# copy dependenies
COPY pyproject.toml /ui/pyproject.toml
COPY ui/__about__.py /ui/ui/__about__.py
COPY README.md /ui/README.md

# install as a package
RUN pip install --upgrade pip && \
    pip install /ui/

# copy code
COPY . /ui

WORKDIR /ui
EXPOSE 8501

# cmd for running the API
CMD ["python", "-m", "streamlit", "run", "ui/webapp.py"]
