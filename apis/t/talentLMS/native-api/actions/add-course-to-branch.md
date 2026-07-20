# Add Course to Branch with TalentLMS

Adds a course to a branch in TalentLMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/branch-courses`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Add Course to Branch](https://documenter.getpostman.com/view/31867199/2sAY548Kou#add-course-to-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch_id` | body | `number` | yes | Numeric branch ID. |
| `course_id` | body | `number` | yes | Numeric course ID. |
