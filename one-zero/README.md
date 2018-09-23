# one zero dgraph cluster

## How to Run

```code
docker-compose up -d
```

## load data

* download data (or use local)

```code
wget "https://github.com/dgraph-io/tutorial/blob/master/resources/1million.rdf.gz?raw=true" -O 1million.rdf.gz -q
```

* copy data

```code
docker cp 1million.rdf.gz one-zero_server_1_1:/dgraph/
```

* load data

```code
dgraph live -r 1million.rdf.gz --zero=zero:5080 -c 1

```