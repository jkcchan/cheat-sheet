# Cheat Sheet
[Alexa Skills Kit](#alexa-skills-kit)
[Rails](#rails)
[MySQL](#mysql)
## Alexa Skills Kit
### Bug - `ask dialog` returning `[Error]`
[Error]: Failed to simulate dialog. The skill that you are trying to simulate has not been created or cloned. If this is a new skill, please try creating and deploying the skill in your project first. If this is an existing skill, please try cloning the skill in your project first. You can also specify the skill id explicitly via the skill-id option.
1. make sure `ask clone` gives the right skills
2. if not, make sure the correct version of node is being used `nvm use ...`
3. if not, ensure  the env variable `ASK_DEFAULT_PROFILE` is right 


## Rails
### New app with PostgreSQL
`rails new myapp --database=postgresql`
## MySQL
### drop multiple columns
alter table TableName
    drop Column1, drop Column2

### rename column
ALTER TABLE sites CHANGE MainImageSplitBackgroundColour MainImageSplitBackgroundColor VARCHAR(255);

### alter table add foreign key
ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID); 

### set values to column of different table
UPDATE table_name1 
    SET column1 = (
        SELECT column2
        FROM table_name2
        WHERE table_name1.id = table_name2.id
    );

### drop foreign key
    ALTER TABLE `custom_links`
	DROP FOREIGN KEY `custom_links_ibfk_1`;

### add not null
ALTER TABLE Persons
MODIFY Age int NOT NULL; 

### remove not null
alter table table_name modify column foo int;