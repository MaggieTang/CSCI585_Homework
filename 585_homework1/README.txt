I. Student can register the coding class and project. They also can borrow at most 4 books from the library and need to return in 2 weeks. 
1. The student entity include the information with student id which is primary key, student name and etc. is detailed information for student.
2. The library entity constains many books, and the book entity need to record the type(since student want to borrow coding books), rent date and return date to make sure student return the book in 2 weeks. And the officer can also can use student_id to check how many book_id is related. This can make sure student just rent at most 4 books.
3. The registration entity is related with student, projects, coding_classes,fee and schedule entity. When student register the whole course, they need to pay the bill, and their data will be added in to the data of project and class. And students can get a schedule with the all the information about the course(include when and where). 

II. The projects and coding_classes entity have more detailed information, and the project_setting and class_setting entity as a role to connect to other entity.
1. project_setting entity show that project can shows which controller and faculty is needed, the time of instructor's teaching(record for payment) and which group is in this project.
2. class_setting entity show that which textbook and faculty is needed, the time of instructor's teaching(record for payment) in this class.

III. The Instructor teach coding classes and oversee the projects, And finally they will get paid.
1. The instructor is a kind of faculty, so I use faculty_id as primary key. As we pointed in II part, this entity is related with project_setting and class_setting entity.
2. And they will paid finally, so Instructor entity is also related with payment entity which is recorded for their salary, which is also depend on their teacing time and project oversee time.

IV. Projects are done in shared fashion, ie. as a group. Students would sit around large, square, numbered tables (1,2..) assigned to them, to work on projects; at the start of the term, each table would be provided a big plastic storage box containing all the parts for the project the students will work on; at the end of the term, students will return all the parts presumably in good working order, otherwise they would be charged for damaged items.
There are several rooms that will be available for the classes and projects - students will be provided a schedule that will list where and when these will be.
1. The entity of group record the student_id to make sure one group have at least 1 and at most 4 students.
2. The table entity record the controller students used in the project. Since it need to be returned in good working order, so it can be connected to table where student is muted.
3. The schedule entity have the information of when and where to take the course, so it include the room_id. 
4. The room have many tables, so the room entity is related with tabbles entity.

V. The owners of the institution plan to order project parts from several online suppliers (such as SparkFun, adafruit etc.) - there is expected to be multiple orders placed with multiple vendors, to procure all the items.
1. organizer need to order from suppliers,  the relationship between oder and supplier is many to many. And one order can have multiple electronic parts.

VI. At the end of the curriculum, students will be required to rate their instructors, courses, and projects, using a single score for each (one to five stars).
1. The rating entity is related with student, instructor, class, project entity.


