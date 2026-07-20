# Search And Sort Courses with Teachlr Organizations

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/available`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Search And Sort Courses](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Word or phrase to search in course title, subtitle, or description. |
| `sort` | query | `string` | yes | Course field to sort by. |
| `ord` | query | `string` | no | Sort direction. |
