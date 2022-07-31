# lambda-layers
Lambda Layers

How to Create
Wrap the file inside a folder named "python" make zip. create a layer and name it as validationLayer. use python 3.8 & 3.9

How to consume
import json
import account_validation as validationLayer

def lambda_handler(event, context):

    print(event['AccNo'])
    validationResult = validationLayer.ValidateAccount(event['AccNo'])
    print(validationResult)

    return {
        'statusCode': 200,
        'body': 'done'
    }

