# Get Search Context By Spec with Sourcegraph

Retrieves a search context from Sourcegraph by spec.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Get Search Context By Spec](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.spec` | body | `string` | no | The search context spec, such as global or @user/context-name. |
