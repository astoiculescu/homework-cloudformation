# homework-cloudformation

Am creat template.yaml cu template-ul pt cloudformation

Am creat stack-ul cu ajutorul template-ului folosind comanda:
aws cloudform create-stack --stack-name homework-cloudformation-s3 --template-body file://template.yaml

Am creat fisierul bucket_policy.json si apoi am setat policy cu comanda:
aws s3api put-bucket-policy --bucket homework-cloudform --policy file:/tmp/bucket_policy.json

Am creat index.html si error.html si incarcat in bucket cu comanda:
aws s3 sync ./ s3://homework-cloudform
