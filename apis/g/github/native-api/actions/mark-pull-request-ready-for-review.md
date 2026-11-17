# Mark Pull Request Ready for Review with GitHub

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Mark Pull Request Ready for Review](https://docs.github.com/en/graphql/reference/mutations#markpullrequestreadyforreview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The pull request's GraphQL node ID (node_id from the REST API). |
