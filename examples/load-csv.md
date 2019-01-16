# Examples

## Loading data into Druid from CSV file

The files _meetup.csv_ and _ingest-csv.json_ and the commands to load a CSV are taken from [this article](https://cleanprogrammer.net/loading-data-into-druid-from-csv-file/).

The only modification is in the section _ioConfig_ in _ingest-csv.json_:

```json
"ioConfig": {
  "type": "index",
  "firehose": {
    "type": "local",
    "baseDir": "/var",
    "filter": "meetup.csv"
  },
  "appendToExisting": false
}
```
where the _baseDir_ is the directory where the example file is loaded.
