# File Metadata Microservice

![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)


File Metadata Microservice is the 5th, and final, project for FreeCodeCamp *Back End Development and APIs* course. The program
utilizes **multer** to handle the file uploaded. The handled data will then be displayed to the user via a JSON response.

🙏 Credits
---
![FreeCodeCamp](https://img.shields.io/badge/Freecodecamp-%23123.svg?&style=for-the-badge&logo=freecodecamp&logoColor=green)

Everything **not** written by me has been cloned from [this GitHub repository](https://github.com/freeCodeCamp/boilerplate-project-filemetadata/).

The default README that comes with the cloned repository:
> This is the boilerplate for the File Metadata Microservice project. Instructions for building your project can be found at https://www.freecodecamp.org/learn/apis-and-microservices/apis-and-microservices-projects/file-metadata-microservice

Here is the solution I wrote for this project:
```
const multer  = require('multer')
const upload  = multer({ dest: "uploads/" });

app.post("/api/fileanalyse", upload.single("upfile"), function(req, res)
{
  try
  {
    res.json({
      name: req.file.originalname,
      type: req.file.mimetype,
      size: req.file.size
    });
  }
  catch(error)
  {
    console.error(error);
  }
});
```



