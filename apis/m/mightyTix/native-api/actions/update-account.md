# Update Account with Mighty Tix

Updates account details in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Update Account](https://mightytix.com/docs/admin-api#mutation-updateAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | AccountInput object from the Mighty Tix Admin GraphQL docs. |
