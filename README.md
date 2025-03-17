# Trading System using Go

A simple trading system that simulates the order process, including:
- Creating an order
- Maintaining an order book
- Matching orders within the order book

## Tech Stack
- **Backend Server**: Go
- **Message Broker**: Kafka
- **In-Memory Storage**: Redis (for the order book)
- **Database**: PostgreSQL

---

## Running the Application

To run the application, use the following command. Ensure you have [Docker](https://www.docker.com/) installed on your system.

```bash
docker-compose up
```

---

## API Endpoints

### Create Order

#### Endpoint
```bash
POST http://localhost:8000/create-order
```

#### Request Body

**Creating an Ask (Sell) Order**
```json
{
    "user_id": 1000000,
    "order_type": 4,
    "type": "ask",
    "price": 100,
    "volume": 150,
    "buying_pair": "usd",
    "selling_pair": "btc"
}
```

**Creating a Bid (Buy) Order**
```json
{
    "user_id": 1000000,
    "order_type": 4,
    "type": "bid",
    "price": 100,
    "volume": 150,
    "buying_pair": "usd",
    "selling_pair": "btc"
}
```

---

### Get Orders

#### Endpoint
```bash
GET http://localhost:8000/get-orders
```

---



