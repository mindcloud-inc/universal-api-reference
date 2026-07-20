# Archive space with Platrum

Archives a knowledge space in Platrum and deletes its articles.

## Endpoint

- **Method:** `POST`
- **Path:** `/wiki/api/space/archive`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [Archive space](http://api.docs.platrum.ru/modules/wiki/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Space ID to archive. |
