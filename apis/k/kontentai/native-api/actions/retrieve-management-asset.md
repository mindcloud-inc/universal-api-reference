# Retrieve management asset with Kontent.ai

Retrieves an asset from your Kontent.ai environment.

## Endpoint

- **Method:** `GET`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/assets/:asset_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Retrieve management asset](https://kontent.ai/learn/docs/apis/management-api-v2/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_identifier` | path | `string` | yes | Kontent.ai asset identifier, such as the asset codename or ID accepted by the Management API. |
