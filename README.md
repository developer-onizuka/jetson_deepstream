```
$ xhost +
access control disabled, clients can connect from any host
$ sudo docker run -it --rm --net=host --runtime nvidia  -e DISPLAY=$DISPLAY -w /opt/nvidia/deepstream/deepstream-5.1 -v /tmp/.X11-unix/:/tmp/.X11-unix --device /dev/video0:/dev/video0:mwr nvcr.io/nvidia/deepstream-l4t:5.1-21.02-samples
```

```
root@nano:/opt/nvidia/deepstream/deepstream-5.1# # deepstream-app -c samples/configs/deepstream-app/source1_usb_dec_infer_resnet_int8.txt 
```
