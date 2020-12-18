## Project Setup
 - run `cp include/config.h.example include/config.h` and set your values in `include/config.h`
 - before building please use `git submodule update --init --recursive`
 - to fix code highlighting component `${workspaceFolder}/components/esp-google-iot/iot-device-sdk-embedded-c/include` should be added to `includeDir` list

## manual keys generation
```
mkdir -p certs
openssl ecparam -genkey -name prime256v1 -noout -out certs/ec_private.pem
openssl ec -in certs/ec_private.pem -pubout -out certs/ec_public.pem 
```

## Additional info
This project uses https://github.com/espressif/esp-google-iot submodule as componnent