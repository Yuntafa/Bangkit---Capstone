# Bangkit---Capstone
# API's Documentation
## GET get-eggs-by-phase/{phase}
Retrieves a Egg data by its Phase // Mengambil data Telur berdasarkan Fase-nya

Parameters :
- `phase` (path parameter) : The Phase of the egg // Fase telur

Response :
The response will contain the following fields // Responnya bakal seperti dibawah :
- `status` (string): The status of the response ("success" or "fail"). // Status respon berhasil atau gagal
- `eggs` (object): The Eggs information with the specified phase, including the following details // Informasi telur dengan fase yang ditentukan, termasuk detail berikut :
    - `id` (number): The ID of the Egg // ID Telur.
    - `additionalInfo` (string): To add additional information by the user // Untuk menambahkan keterangan tambahan oleh user 
    - `description` (string): The description of the Egg // Deskrpisi Telur.
    - `detectionTimestamp` (timestamp): Detection time // Waktu deteksi.
    - `fertilization` (boolean): Fertil or Infertil // Fertil atau Infertil.
    - `imageRef` (reference): Get the egg detection images from the Egg-Images collection. // Mendapatkan gambar hasil deteksi telur dari collection Egg-Images.
    - `labelRef` (reference): Get label from the labels collection // Mendapatkan data (label) dari Collection labels
    - `phasse` (string): Phase of the eggs // Fase dari telurnya
    - `userId` (string): User Id of the egg data // Id User dari data telurnya


Example Request // Contoh Requestnya: 
```
GET /get-eggs-by-phase/Embrio
```

```
{
    "status": "success",
    "eggs": [
        {
            "id": "detection-id",
            "additionalInfo": "keterangan_tambahan",
            "description": "deskripsi hasil deteksi",
            "detectionTimestamp": {
                "_seconds": 1700773200,
                "_nanoseconds": 337000000
            },
            "fertilization": "Fertil",
            "imageRef": {
                "_firestore": {
                    "projectId": "avid-lock-405816"
                },
                "_path": {
                    "segments": [
                        "Egg-Images",
                        "egg-images-id"
                    ]
                },
                "_converter": {}
            },
            "labelRef": {
                "_firestore": {
                    "projectId": "avid-lock-405816"
                },
                "_path": {
                    "segments": [
                        "labels",
                        "label-id"
                   ]
                },
                "_converter": {}
            },
            "phase": "Embrio",
            "userId": "[user-id]"
        }
    ]
}
