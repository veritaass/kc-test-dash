FROM python:3.10.0-bullseye

# RUN pip install dash dash_bootstrap_components dash_admin_components pandas scikit-learn pyparsing statsmodels dash_bio python-dotenv

RUN pip install --upgrade pip
RUN pip install dash flask python-keycloak 
#  1 dash
#  2 flask
#  3 python-keycloak
#RUN pip install -r requirements.txt

RUN mkdir /data

COPY . /data/dash
WORKDIR /data/dash
EXPOSE 8088
#ENTRYPOINT ["python","index.py"]
CMD ["python", "-m", "flask_keycloak.examples.dash_example", "flask_keycloak/examples/keycloak.json"]

