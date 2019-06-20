# target-classifier

## To build

From this comprehension directory:

```
$ s2i build . seldonio/seldon-core-s2i-python3:0.7 dwhitena/target-classifier:v0.1

$ docker push dwhitena/target-classifier:v0.1
```

## API

Example request:

```
$ curl -X POST -H 'Content-Type: application/json' \
    -d '{"data": {"names": ["message"], "ndarray": ["What does the Bible say about tattoos"]}}' \
    http://35.201.10.193/seldon/default/target-classifier/api/v0.1/predictions
```

Example response:

```
{
  "meta": {
    "puid": "621fkb3colis0o0h0b19jau01j",
    "tags": {
    },
    "routing": {
    },
    "requestPath": {
      "classifier": "dwhitena/target-classifier:v0.1"
    },
    "metrics": []
  },
  "strData": "True"
}
```
