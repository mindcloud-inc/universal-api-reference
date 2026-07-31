# Fetch Random Excuses By Category with Excuser

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/excuse/:category/:count`
- **Base URL:** `https://excuser-three.vercel.app`
- **Official documentation:** [Fetch Random Excuses By Category](https://excuser-three.vercel.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | path | `list<string>` | yes | Provider-documented excuse category. Accepted values: `children`, `college`, `developers`, `family`, `funny`, `gaming`, `office`, `party`, `unbelievable`. |
| `count` | path | `number` | yes | Number of random excuses to return. |
