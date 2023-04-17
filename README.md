# ZENCLASS-MONGODB
Zenclass MongoDB
// To find all month

// db.topics.aggregate(
//     [
//       {
//         $project:
//           {
                  
//             Month: { $month: "$topicDate" }
//           }
//       }
//     ]
//   )


// 1)Find all the topics and tasks which are thought in the month of October


// db.tasks.find({ "$expr": { "$eq": [{ "$month": "$taskDate" }, 10] } })
// db.topics.find({ "$expr": { "$eq": [{ "$month": "$topicDate" }, 10] } })

// 2)Find all the company drives which appeared between 15 oct-2020 and 31-oct-2020

// db.company_drives.find(
//     { appearedDate: { $gte: new Date("2022-10-15"), 
//     $lte: new Date("2023-10-31") 
//   } 
// })

// 3)Find all the company drives and students who are appeared for the placement

// db.company_drives.find()

// db.users.find({
//     appearedplacement:'true'
//     })

// 4)  Find the number of problems solved by the user in codekata

// db.users.aggregate([
//     { $lookup:
//         {
//            from: "codekata",
//            localField: "UserName",
//            foreignField: "UserName",
//            as: "Name"
//         }
//     }
// ]).pretty();

// 5)Find all the mentors with who has the mentee's count more than 15


// db.mentors.find( { Menteecount: { $gt: 10 } } )









