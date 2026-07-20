# Upsert management asset with Kontent.ai

Upserts an asset in Kontent.ai by external ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/assets/external-id/:external_id`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Upsert management asset](https://kontent.ai/learn/docs/apis/management-api-v2/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | path | `string` | yes | External ID used to upsert the Kontent.ai asset. |
| `body` | body | `object` | yes | JSON request body for upserting a Kontent.ai management asset. |
