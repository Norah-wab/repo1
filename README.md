# project description: 
the purpose of this project to give a email and password then provide jwt and authroize based on it. 

# API url is: 
ab5da74c36291494292941449a1a0977-1410223144.eu-west-2.elb.amazonaws.com 

example commands:- 
export TOKEN=`curl -d '{"email":"<EMAIL>","password":"<PASSWORD>"}' -H "Content-Type: application/json" -X POST ab5da74c36291494292941449a1a0977-1410223144.eu-west-2.elb.amazonaws.com/auth  | jq -r '.token'`

curl --request GET 'ab5da74c36291494292941449a1a0977-1410223144.eu-west-2.elb.amazonaws.com/contents' -H "Authorization: Bearer ${TOKEN}" | jq