#mysql command
##CREATE DATABASE 数据库名;
CREATE DATABASE [IF NOT EXISTS] database_name
DROP DATABASE  [IF NOT EXISTS] <database_name>;        -- 直接删除数据库，检查是否存在
FLOAT/DOUBLE
#建立資料表
create table table_name(
no varchar(10) primary key,
name varchar(20),
age int(2),
sex varchar(5)
);
DROP TABLE [IF EXISTS] table_name;  -- 会检查是否存在，如果存在则删除

INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);

SELECT column1, column2, ...
FROM table_name
WHERE condition;

UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

DELETE FROM table_name
WHERE condition;

SELECT column1, column2, ...
FROM table1
WHERE condition1
UNION
SELECT column1, column2, ...
FROM table2
WHERE condition2
[ORDER BY column1, column2, ...];

SELECT column1, column2, aggregate_function(column3)
FROM TABLE_NAME
WHERE condition
GROUP BY column1, column2;

SELECT column1, column2, ...
FROM table_name
WHERE column_name RLIKE 'pattern';

ALTER TABLE table_name
ADD COLUMN new_column_name datatype;

alter table table_name ADD column ABD int;
alter table table_name  modify table_name table_name2 vachar(255);
ALTER TABLE table_name
DROP COLUMN column_name;
ALTER TABLE table_name
ADD PRIMARY KEY (column_name);
ALTER TABLE child_table
ADD CONSTRAINT fk_name
FOREIGN KEY (column_name)
REFERENCES parent_table (column_name);
ALTER TABLE old_table_name
RENAME TO new_table_name;

CREATE INDEX idx_name ON students (name);
ALTER TABLE table_name
ADD INDEX index_name (column1 [ASC|DESC], column2 [ASC|DESC], ...);
DROP INDEX index_name ON table_name;
ALTER TABLE table_name
DROP INDEX index_name;
CREATE UNIQUE INDEX index_name
ON table_name (column1 [ASC|DESC], column2 [ASC|DESC], ...);
