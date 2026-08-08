# Get Job ID by External ID with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-jobs-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Get Job ID by External ID](https://integration-docs.xoi.io/schemas/jobs/#getjobidbyexternalidinput)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.externalId` | body | `string` | yes | External ID associated with the XOi job. |
