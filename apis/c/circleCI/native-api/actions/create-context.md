# Create Context with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/context`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Context](https://circleci.com/docs/api/v2/#tag/Context/operation/createContext)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The context name. |
| `owner` | body | `object` | yes | Context owner object with organization id or slug and type. |
