CREATE TABLE User(
  user_id varchar(50),
  age int
);

CREATE TABLE asset(
  item varchar(255),
  user_id varchar(50)
 );
  
INSERT INTO User(user_id, age) VALUES 
('wildan', 27),
('zaki', 25);

INSERT INTO asset(item, user_id) VALUES
('notebook', 'wildan'),
('bag', 'wildan'),
('notebook', 'zaki'),
('bag', 'zaki'),
('mobile phone', 'zaki');


SELECT DISTINCT item FROM asset;
SELECT user.user_id, asset.item FROM user LEFT JOIN asset ON asset.user_id = user.user_id;