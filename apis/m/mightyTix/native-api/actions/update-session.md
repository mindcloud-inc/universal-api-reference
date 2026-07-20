# Update Session with Mighty Tix

Updates an existing session in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Update Session](https://mightytix.com/docs/admin-api#mutation-updateOneSession)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | UpdateOneSessionInput object from the Mighty Tix Admin GraphQL docs. |
