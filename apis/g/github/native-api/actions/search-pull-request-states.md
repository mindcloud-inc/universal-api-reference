# Search Pull Request States with GitHub

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Search Pull Request States](https://docs.github.com/en/graphql/reference/queries#search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.q` | body | `string` | yes | GitHub search qualifiers, for example: is:pr is:open author:@me archived:false |
