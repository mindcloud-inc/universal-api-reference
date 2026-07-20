# List Contacts With Relationship Metrics with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contacts/List`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [List Contacts With Relationship Metrics](https://ipaas.sigparser.com/v1#post-api-contacts-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expand_relationship_metrics_type` | body | `string` | no | Which contacts to include in relationship_metrics: INTERNAL, EXTERNAL, or ALL. |
| `page` | body | `number` | no | Page 1 is the first page of results. |
| `take` | body | `number` | no | How many contacts per page. Max 200. |
| `expand_relationship_metrics_history` | body | `boolean` | no | Expand the history within the relationship metrics. |
