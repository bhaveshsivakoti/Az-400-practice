export GH_USERNAME='bhaveshsivakoti'

export GH_TOKEN=''

export GH_IMAGE='helloworld'

export GH_VERSION='latest'

echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag $GH_IMAGE:$GH_VERSION ghcr.io/$GH_USERNAME/helloworld:1.0.1

docker push ghcr.io/bhaveshsivakoti/helloworld:1.0.1