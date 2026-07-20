# Design Interior with ModelsLab

Creates an interior design image in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/interior/make`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Design Interior](https://docs.modelslab.com/interior-api/interior)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | no | Interior source image URL. |
| `prompt` | body | `string` | no | Interior design style prompt. |
