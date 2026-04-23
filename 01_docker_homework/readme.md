C:\Users\79136\docker_homework>docker build --no-cache -t netology-ml:netology-ml .
[+] Building 109.5s (9/9) FINISHED                                                                                                                                     docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                                                                   0.0s
 => => transferring dockerfile: 665B                                                                                                                                                   0.0s
 => [internal] load metadata for docker.io/continuumio/miniconda3:latest                                                                                                               0.8s
 => [auth] continuumio/miniconda3:pull token for registry-1.docker.io                                                                                                                  0.0s
 => [internal] load .dockerignore                                                                                                                                                      0.0s
 => => transferring context: 2B                                                                                                                                                        0.0s
 => [1/4] FROM docker.io/continuumio/miniconda3:latest@sha256:b002473017c77d4b8bad6f8c49747e0298c37419a5ec69ca37ebe36d09ee417a                                                         0.0s
 => => resolve docker.io/continuumio/miniconda3:latest@sha256:b002473017c77d4b8bad6f8c49747e0298c37419a5ec69ca37ebe36d09ee417a                                                         0.0s
 => CACHED [2/4] WORKDIR /app                                                                                                                                                          0.0s
 => [3/4] RUN echo '#!/bin/bash' > /app/1.sh &&     echo 'echo "Hello Netology"' >> /app/1.sh &&     chmod +x /app/1.sh                                                                0.3s
 => [4/4] RUN pip install mlflow boto3 pymysql                                                                                                                                        61.0s
 => exporting to image                                                                                                                                                                47.2s
 => => exporting layers                                                                                                                                                               33.3s
 => => exporting manifest sha256:323ebb11dcdea04bb7b59922d4bf66a582410dd1f70f83a2ea1ccb4db4297378                                                                                      0.0s
 => => exporting config sha256:73d82b48ffca1bb815ddd1742bd02d9e55f038ac5cadc99ba59f446110d25c7b                                                                                        0.0s
 => => exporting attestation manifest sha256:af8a49cf7f4891bfa614cd13872cd96d345b3c12eea01317f0faf1e74a08f068                                                                          0.0s
 => => exporting manifest list sha256:af47ec1d7075619a46e55d857eaa220c0ad9ee9b869b623656d2662ecb3a2ed4                                                                                 0.0s
 => => naming to docker.io/library/netology-ml:netology-ml                                                                                                                             0.0s
 => => unpacking to docker.io/library/netology-ml:netology-ml                                                                                                                         13.7s

View build details: docker-desktop://dashboard/build/desktop-linux/desktop-linux/0tqgwhrai9c3isalf0ff1xhs8

C:\Users\79136\docker_homework>docker run --rm netology-ml:netology-ml
Hello Netology