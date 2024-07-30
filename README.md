To run it on your local machine follow these steps
```
1. git clone https://github.com/coderpawan/Task-Manager.git
2. setup env variables
- APP_URL  (the live url of the app where its hosted on eg https://task-manager-3vbi.onrender.com/)
- EMAIL_HOST (for nodemailer)
- EMAIL_USER (for nodemailer)
- EMAIL_PASS (for nodemailer)
  const transporter = nodemailer.createTransport({
    host: process.env.EMAIL_HOST,
    port: 587,
    auth: {
        user: process.env.EMAIL_USER,
        pass: process.env.EMAIL_PASS
    }
});
- JWT_LIFETIME (for JWT eg 5d)
- JWT_SECRET (for JWT. You can generate one from https://jwtsecret.com/  256bit)
- MONGO_URI (for mongoose/mongodb driver connection eg mongodb+srv://YourProfile:YourPassword@nodeexpressproject.of3osfz.mongodb.net/TASK-MANAGER?retryWrites=true&w=majority)
3. npm run setup-production
4. npm run start
```


### Features of the app

- Boards
  - [x] Clicking different boards in the sidebar will change to the selected board.
  - [x] Clicking "Create New Board" in the sidebar opens the "Add New Board" modal.
  - [x] Clicking in the dropdown menu "Edit Board" opens up the "Edit Board" modal where details can be changed.
  - [x] Columns are added and removed for the Add/Edit Board modals.
  - [x] Deleting a board deletes all columns and tasks and requires confirmation.
- Columns
  - [x] A board needs at least one column before tasks can be added.
  - [x] Clicking "Add New Column" opens the "Edit Board" modal where columns are added.
- Tasks
  - [x] Adding a new task adds it to the bottom of the relevant column.
  - [x] Updating a task's status will move the task to the relevant column. If you're taking on the drag and drop bonus, dragging a task to a different column will also update the status.
