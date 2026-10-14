# speedtest
speedtest网络测速

wget https://github.com/ZQYKing/speedtest/releases/download/v1.0.1/librespeed-5.2.5.tar

docker load -i  librespeed-5.2.5.tar

docker run -d \
  --name librespeed \
  --restart unless-stopped \
  -p 8080:8080 \
  -e WEBPORT=8080 \
  -e MODE=standalone \
  -e TITLE="香港三网优化网络测速" \
  -e TELEMETRY=false \
  librespeed:5.2.5
