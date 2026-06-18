#schema data
1.FARMER TABLE:
Farmer

id BIGINT PRIMARY KEY

name VARCHAR(100)

phone VARCHAR(15)

village VARCHAR(100)

district VARCHAR(100)

state VARCHAR(100)

created_date TIMESTAMP

updated_date TIMESTAMP

2.crop table
Crop

id BIGINT PRIMARY KEY

crop_name VARCHAR(100)

season VARCHAR(50)

market_price DECIMAL(10,2)

farmer_id BIGINT

created_date TIMESTAMP

updated_date TIMESTAMP

3.FOREIGN KEY (farmer_id)
REFERENCES Farmer(id)

4.Market Table :

Market

id BIGINT PRIMARY KEY

crop_name VARCHAR(100)

current_price DECIMAL(10,2)

market_name VARCHAR(100)

updated_date TIMESTAMP


ER DIAGRAM:

Farmer
-------
id
name
phone
village
district
state

      1
      |
      |
      *
Crop
-------
id
crop_name
season
market_price
farmer_id
