FROM python:3

RUN pip install flask && \
    pip install flask-sqlalchemy && \
    pip install py-kim && \
    mkdir -p /opt/code

workdir /opt/code/ \
ADD . /opt/code
RUN python setup.py develop

Expose 5000 \
ENV FLASK_APP /opt/code/example/app.py
CMD ["flask", "run", "--port", "5000", "--host", "192.168.0.130"]


