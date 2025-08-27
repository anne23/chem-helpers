FROM python:3.13-trixie

RUN git clone https://github.com/ParmEd/ParmEd.git /ParmEd
WORKDIR /ParmEd
RUN pip install numpy setuptools
RUN python setup.py install
