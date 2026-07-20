# Create Bucket with Google Cloud Storage

Creates a new bucket in Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/v1/b`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Create Bucket](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Globally unique bucket name. |
| `location` | body | `list<string>` | no | Bucket location, such as US, EU, or a region. Accepted values: `AFRICA-SOUTH1`, `ASIA`, `ASIA-EAST1`, `ASIA-EAST2`, `ASIA-NORTHEAST1`, `ASIA-NORTHEAST2`, `ASIA-NORTHEAST3`, `ASIA-SOUTH1`, `ASIA-SOUTH2`, `ASIA-SOUTHEAST1`, `ASIA-SOUTHEAST1-A`, `ASIA-SOUTHEAST1-B`, `ASIA-SOUTHEAST1-C`, `ASIA-SOUTHEAST2`, `ASIA-SOUTHEAST3`, `ASIA1`, `AUSTRALIA-SOUTHEAST1`, `AUSTRALIA-SOUTHEAST2`, `EU`, `EUR4`, `EUR5`, `EUR7`, `EUR8`, `EUROPE-CENTRAL2`, `EUROPE-NORTH1`, `EUROPE-NORTH2`, `EUROPE-SOUTHWEST1`, `EUROPE-WEST1`, `EUROPE-WEST1-B`, `EUROPE-WEST1-C`, `EUROPE-WEST1-D`, `EUROPE-WEST10`, `EUROPE-WEST12`, `EUROPE-WEST2`, `EUROPE-WEST3`, `EUROPE-WEST4`, `EUROPE-WEST6`, `EUROPE-WEST8`, `EUROPE-WEST9`, `ME-CENTRAL1`, `ME-CENTRAL2`, `ME-WEST1`, `NAM4`, `NORTHAMERICA-NORTHEAST1`, `NORTHAMERICA-NORTHEAST2`, `NORTHAMERICA-SOUTH1`, `SOUTHAMERICA-EAST1`, `SOUTHAMERICA-WEST1`, `US`, `US-CENTRAL1`, `US-CENTRAL1-A`, `US-CENTRAL1-B`, `US-CENTRAL1-C`, `US-CENTRAL1-F`, `US-EAST1`, `US-EAST4`, `US-EAST4-A`, `US-EAST4-B`, `US-EAST4-C`, `US-EAST5`, `US-EAST5-A`, `US-EAST5-B`, `US-EAST5-C`, `US-SOUTH1`, `US-WEST1`, `US-WEST2`, `US-WEST3`, `US-WEST4`, `US-WEST4-A`, `US-WEST4-B`, `US-WEST4-C`. |
| `storageClass` | body | `list<string>` | no | Default storage class for new objects. Accepted values: `ARCHIVE`, `COLDLINE`, `NEARLINE`, `RAPID`, `STANDARD`. |
