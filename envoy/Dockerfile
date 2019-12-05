FROM envoyproxy/envoy:latest
RUN  apt-get update && apt-get -y install gettext-base moreutils
RUN  rm /dev/shm/envoy_shared_memory_0
CMD /bin/bash -c "echo $CONFIG > /etc/envoy/envoy.json && envsubst < /etc/envoy/envoy.json | sponge /etc/envoy/envoy.json && exec envoy -c /etc/envoy/envoy.json"
