
-- Question1
```
SQL
CREATE TABLE professors(
    ssn int,
    PRIMARY KEY (ssn)
);

CREATE TABLE courses (
    courseid int,
    PRIMARY KEY (courseid)
);

CREATE TABLE teaches (
    semester int,
    ssn int,
    courseid int,
    PRIMARY KEY (ssn, courseid),
    FOREIGN KEY (ssn) REFERENCES professors
    FOREIGN KEY (courseid) REFERENCES courses
);

```


-- Question3

```
SQL
CREATE TABLE professors(
    ssn int,
    PRIMARY KEY (ssn)
);

CREATE TABLE courses (
    courseid int,
    PRIMARY KEY (courseid)
);

CREATE TABLE teaches (
    semester int,
    ssn int NOT NULL,
    courseid int NOT NULL,
    PRIMARY KEY (ssn, courseid),
    FOREIGN KEY (ssn) REFERENCES professors
    FOREIGN KEY (courseid) REFERENCES courses
);

```

-- Question5

```
SQL
CREATE TABLE professors (
    ssn int,
    PRIMARY KEY (ssn)
);

CREATE TABLE courses (
    courseid int,
    PRIMARY KEY (courseid)
);

CREATE TABLE teaches (
    semesterid int,
    ssn int NOT NULL,
    courseid int NOT NULL,
    PRIMARY KEY (semesterid),
    FOREIGN KEY (ssn) REFERENCES professors,
    FOREIGN KEY (courseid) REFERENCES courses
);

```

-- Question6

```
SQL
CREATE TABLE professors (
    ssn int,
    PRIMARY KEY (ssn)
);

CREATE TABLE groups (
    groupid int,
    PRIMARY KEY (groupid)
);

CREATE TABLE member (
    ssn int,
    groupid int,
    FOREIGN KEY (ssn) REFERENCES professors,
    FOREIGN KEY (groupid) REFERENCES groups
);

CREATE TABLE courses (
    courseid int,
    PRIMARY KEY (courseid)
);

CREATE TABLE teaches (
    semester int,
    groupid int,
    courseid int,
    PRIMARY KEY (groupid, courseid),
    FOREIGN KEY (groupid) REFERENCES groups,
    FOREIGN KEY (courseid) REFERENCES courses
);

```
 
