# Delete Session with Mighty Tix

Deletes an existing session from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Delete Session](https://mightytix.com/docs/admin-api#mutation-deleteOneSession)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | DeleteOneSessionInput object from the Mighty Tix Admin GraphQL docs. |
