# Get Package with HirePOS

Finds a package in HirePOS by package code.

## Endpoint

- **Method:** `GET`
- **Path:** `/Packages`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [Get Package](https://docs.hirepos.com/en/articles/3084161)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PackageCode` | query | `string` | yes | Find a package by its exact HirePOS package code. |
