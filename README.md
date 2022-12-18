Data bucket: 
https://storage.googleapis.com/dotsconnect-data1

Make bucket public:
https://cloud.google.com/storage/docs/access-control/making-data-public#console_1

Install Google Cloud CLI into WSL Linux instance:
https://cloud.google.com/sdk/docs/downloads-interactive#linux-mac

## Watersheds

Source: [National watershed boundary datasets (WBD)](https://nrcs.app.box.com/v/huc/folder/39290322977)

Prep:
* ogr2ogr -t_srs "EPSG:4326" -f FlatGeobuf "/mnt/c/data/wbd/wbdhu12_a_us_september2022.fgb" "/mnt/c/data/wbd/wbdhu12_a_us_september2022.gdb"
* gcloud storage cp /mnt/c/data/wbd/wbdhu12_a_us_september2022.fgb gs://dotsconnect-data1

https://storage.googleapis.com/dotsconnect-data1/wbdhu12_a_us_september2022.fgb