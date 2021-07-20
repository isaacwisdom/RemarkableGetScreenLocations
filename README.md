# RemarkableGetScreenLocations
simple way of grabbing screen coordinates from the reMarkable Tablet

Instructions:
1. Upload [this pdf](https://github.com/isaacwisdom/RemarkableGetScreenLocations/blob/567cb705181f9b5cc0231c3be82ff722ef5540de/Development%20Notes.pdf) to your reMarkable however you'd like (reMarkable desktop app, usb web connections, rmapi...), and open it on your reMarkable.
2. SSH into your RM and run these commands:
```shell
cd
wget https://github.com/isaacwisdom/RemarkableGetScreenLocations/releases/latest/download/GetScreenLocations
chmod +x GetScreenLocations
```
3. With the PDF open on your RM, run the following command:

*For RM1, touchscreen*

```./GetScreenLocations /dev/input/event1 30```

*For RM1, pen*

```./GetScreenLocations /dev/input/event0 30```

*For RM2, touchscreen*

```./GetScreenLocations /dev/input/event2 30```

*For RM1, pen*

```./GetScreenLocations /dev/input/event1 30```

The program will ask you to press each location 5 times and will pause between locations. Be careful to not touch anything during that second, or you can overlap the events. If you need to start over, you can quit with control-C.
