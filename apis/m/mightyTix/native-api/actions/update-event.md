# Update Event with Mighty Tix

Updates an existing event in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Update Event](https://mightytix.com/docs/admin-api#mutation-updateOneEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | UpdateOneEventInput object from the Mighty Tix Admin GraphQL docs. |
