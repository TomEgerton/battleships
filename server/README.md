# Battleships

Game server code for distributed battleships. The client is for reference only, but it contains all the information, 
including a lot of comments and explanations, to create a client of your own.

### Create protobuf and gRPC files

From within the `app` directory:

`python -m grpc_tools.protoc -I.\protos --python_out=. --grpc_python_out=. msg.proto`

The created pb2 files are checked in to git. This means that the files should be updated when any of the files in
`protos` are changed. Alternatively, a package could be created that contains only the proto files and the generated
pb2 files. For now, this is fine, though.

### Unit tests

The unit tests are best run from within PyCharm. It's straightforward enough to create a new Configuration:
1) Click on the test folder
2) Click on Run | Run (Alt-Shift-F10)
3) Click on 'Unittests in test'

The configuration can now also be chosen in the dropdown menu in the top right corner where the Run / Debug buttons
reside.

The unit tests could use some TLC, tbh.