# Bangkit---Capstone
# API's Documentation
## GET get-eggs-by-phase/{phase}
Retrieves a Egg data by its Phase

Parameters :
phase (path parameter) : The Phase of the egg

Response :
The response will contain the following fields:
- `status` (string): The status of the response ("success" or "fail").
- `phase` (object): The place information with the specified ID, including the following details :
id (number): The ID of the Egg.
additionalInfo (string): Untuk menambahkan catatan tambahan oleh user
description (string): The description of the Egg
