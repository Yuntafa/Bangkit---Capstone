# Bangkit---Capstone
# API's Documentation
## GET get-eggs-by-phase/{phase}
Retrieves a Egg data by its Phase // Mengambil data Telur berdasarkan Fase-nya

Parameters :
- `phase` (path parameter) : The Phase of the egg // Fase telur

Response :
The response will contain the following fields // Responnya bakal seperti dibawah :
- `status` (string): The status of the response ("success" or "fail"). // Status respon berhasil atau gagal
- `eggs` (object): The place information with the specified ID, including the following details :
    - `id` (number): The ID of the Egg.
    - `additionalInfo` (string): Untuk menambahkan catatan tambahan oleh user
    - `description` (string): The description of the Egg
    - `detectionTimestamp` (timestamp): 
