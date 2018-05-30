build:
	protoc --proto_path=. --go_out=. --micro_out=. \
	  proto/consignment/consignment.proto
	GOOS=linux GOARCH=amd64 go build
	docker build -t consignment-service .

run: 
	docker run -p 8011:50051 consignment-service
