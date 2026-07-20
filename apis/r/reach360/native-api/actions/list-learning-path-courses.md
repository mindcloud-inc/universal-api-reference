# List Learning Path Courses with Reach360

Retrieves all courses in a Reach360 learning path.

## Endpoint

- **Method:** `GET`
- **Path:** `/learning-paths/:learningPathId/courses`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [List Learning Path Courses](https://www.articulatesupport.com/article/Reach-360-Learning-Paths-API)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `learningPathId` | path | `string` | yes | The learning path ID. |
