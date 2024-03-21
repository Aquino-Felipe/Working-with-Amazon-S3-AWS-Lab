aws s3 mb s3://cafe-lab-test44 --region 'us-west-2'

aws s3 sync ~/initial-images/ s3://cafe-lab-test44/images

aws s3 ls s3://cafe-lab-test44/images/ --human-readable --summarize

arn:aws:sns:us-west-2:654654616299:s3NotificationTopic

aws s3api put-bucket-notification-configuration --bucket cafe-lab-test44 --notification-configuration file://s3EventNotification.json

aws s3api put-object --bucket cafe-lab-test44 --key images/Caramel-Delight.jpg --body ~/new-images/Caramel-Delight.jpg

aws s3api get-object --bucket cafe-lab-test44 --key images/Donuts.jpg Donuts.jpg

aws s3api delete-object --bucket cafe-lab-test44 --key images/Strawberry-Tarts.jpg

aws s3api put-object-acl --bucket cafe-lab-test44 --key images/Donuts.jpg --acl public-read