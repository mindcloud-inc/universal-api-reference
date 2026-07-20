# Create User with Mighty Tix

Creates a new user in Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [Create User](https://mightytix.com/docs/admin-api#mutation-createOneUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input` | body | `object` | yes | CreateOneUserInput object from the Mighty Tix Admin GraphQL docs. |
