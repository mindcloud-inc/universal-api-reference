# Delete User with Mighty Tix

Deletes an existing user from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Delete User](https://mightytix.com/docs/admin-api#mutation-deleteOneUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | DeleteOneUserInput object from the Mighty Tix Admin GraphQL docs. |
