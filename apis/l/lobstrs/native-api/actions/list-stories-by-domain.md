# List Stories by Domain with lobst.rs

Finds stories in lobst.rs by domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [List Stories by Domain](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Submitted URL domain, such as github.com. |
