ansible-playbook s3_localstack.yml

aws --endpoint-url=http://localhost:4566 s3 ls


python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install ansible boto3 botocore


ansible-playbook s3_localstack.yml -e ansible_python_interpreter=$(which python)

aws s3 ls --profile localstack --endpoint-url=http://localhost:4566
