```xml

Table {
	id integer pk increments
	countClient integer
	idImageTable integer > ImageTable.id
	idHall integer *> Hall.id
}

Hall {
	id integer pk increments
	nameHall integer
	basePrice integer
}

ImageTable {
	id integer pk increments
	image text
}

Client {
	id integer pk increments
	name integer
	phoneNumber integer
	hashPassword varchar
}

Schedule {
	id integer pk increments
	idClient integer > Client.id
	idTable integer > Table.id
	dateTime datetime
	countClient integer
}

```