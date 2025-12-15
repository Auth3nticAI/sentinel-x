FROM python:3.10-slim

WORKDIR /app

RUN pip install numpy matplotlib jupyter

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--no-browser", "--allow-root"]
