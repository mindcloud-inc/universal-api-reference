# Research Keywords with SEOTakeoff

## Endpoint

- **Method:** `POST`
- **Path:** `/api/zapier/clusters/research-keywords`
- **Base URL:** `https://api.seotakeoff.com`
- **Official documentation:** [Research Keywords](https://api.seotakeoff.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cluster_id` | body | `string` | yes | Cluster ID to research. |
| `seed_topic` | body | `string` | yes | Topic to research for new keywords. |
| `count` | body | `number` | no | Number of keywords to research, between 5 and 50. |
