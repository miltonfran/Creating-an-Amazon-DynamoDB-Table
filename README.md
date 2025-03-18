<h1>Creating an Amazon DynamoDB Table</h1>

<h2>Description</h2>
we've already created and modified the application and have created and tested the uploading to the S3 bucket, so to get the application fully functional, or at a fully functional stage, the next thing to do is to launch a database.
<br />

<h2>Program walk-through:</h2>

1. Before launching the database, launch an instance ready to use that database so that we can test it as soon as it's done.
- Go over to EC2, and go over to the instances.
- Use the shortcut where I launch a clone of an instance already launched.
- select my employee-directory-app-s3, because that's the most updated version of this application, and go over to actions, images, and templates,  launch more like this.
- Instead of  -s3 to this, write -dynamodb, for the name.
- Scroll down, and make sure that you still using the same key.
- verify if you still using the role
- ensure that the instance launches with a public IP
- Make sure to enable public IP
- we can see that the user data is exactly where it was left, after adding the bucket.
- Now click Launch instance.
- Go ahead and refresh the page, see that two of the checks have passed.
- Select the dynamodb labeled instance and copy its public IP address, to make sure that the application is up and running before proceed.
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742324130/Screenshot_2025-03-17_200839_rugomo.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742324147/Screenshot_2025-03-17_200948_kfimlp.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742324159/Screenshot_2025-03-17_201019_bixnev.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742324163/Screenshot_2025-03-17_203528_axqaz9.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742325072/Screenshot_2025-03-17_203729_y23o9l.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742328386/Screenshot_2025-03-17_203748_hnfvqy.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742328399/Screenshot_2025-03-17_203918_fc9vxu.png"/>
<br />

2. Once the application is successfully running, move forward with creating the database
- Go up to the search bar and type in dynamo and click on the DynamoDB service.
- click Create table
- For the table name, I'm going to put Employees because the application is set up to work with a database named Employees.
- for my partition key, I'm going to put id
- I'm going to keep this type as a string
- all of the default settings can remain
- go ahead and click Create table.
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742330439/Screenshot_2025-03-17_203952_tylhs9.png"/>
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742330575/Screenshot_2025-03-17_204016_jglysq.png"/>
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742330579/Screenshot_2025-03-17_204452_a4jrtd.png"/>
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742330634/Screenshot_2025-03-17_204530_berhjs.png"/>
 <br />

 3. Now that the table is created, instead of adding items directly to this table, test the application again, and make sure I copy the instance's public IP address.
- go over to my instances select the instance that was launched for this and copy its IP address, in a new tab paste that address.
- See that the Employee Directory app is still running, and it is currently an empty directory.
- Go ahead and add an employee to this directory to make sure that everything is connected
- Click Add, and go ahead and put your name here, location, and job title, in addition, select a couple of these options here, just so that we can see what it looks like as everything is added to the table and added to this directory.
- Add employee photo and open, and then once that has all been added, go ahead and click Save.

 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742334859/Screenshot_2025-03-17_205115_lqqvlo.png"/>
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742334862/Screenshot_2025-03-17_205311_knsu2l.png"/>
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742334866/Screenshot_2025-03-17_205516_txm6ys.png"/>
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742334876/Screenshot_2025-03-17_205614_xaf7nh.png"/>
<br />

 4. I want to show that this isn't just something that was added to this location, So, what I will do is show that these items were added to the table and in the S3 bucket.
So starting with S3, I'll go over to S3, and then, I will open up the bucket that I had created.
- we can see, my employee pic has been added, and it's the employee picture that I uploaded.
- Even though it has its own designated name here, this is the object that was uploaded through that application.

 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742336998/Screenshot_2025-03-17_205811_po4tyo.png"/>
 <img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742337193/Screenshot_2025-03-17_205827_cgnem5.png"/>
<br />

5. Go over to DynamoDB, so can view the table, view employee table, and explore the table items, I can also see that my employee items that were added through the directory
-  it shows which badges, name, job titles, location, It shows the name of the object that was uploaded through the directory, and it shows the ID specifically for this table, and the partition key that we established.
- Go back to EC2 and stop the instance so that you are not accruing any additional charges.
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742339172/Screenshot_2025-03-17_205921_yvyakb.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742339203/Screenshot_2025-03-17_210028_gchkwf.png"/>
<img src="https://res.cloudinary.com/dk3bkl3ji/image/upload/v1742339253/Screenshot_2025-03-17_210107_uhiyrc.png"/>




















