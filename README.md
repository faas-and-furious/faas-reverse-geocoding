### ReverseGeocoding

Get address from GPS coordinates

### Build image

```
$ docker build -t lucj/faas-reverse-geocoding .
```

### Service creation

```
$ faas-cli deploy \
  --image lucj/faas-reverse-geocoding \ 
  --name ReverseGeocoding \
  --fprocess="java -jar app-standalone.jar"
```

### Usage

The function can be invoked using the following format:

```
curl -d 'LONGITUDE LATITUDE' http://localhost:8080/function/ReverseGeocoding
```

### Example

```
$ curl -d '7.116703 43.581915' http://localhost:8080/function/ReverseGeocoding
20 Avenue Reibaud, 06600 Antibes, France
```
