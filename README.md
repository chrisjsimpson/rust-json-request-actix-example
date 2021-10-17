# Rust actix json request example

Send a json request to actix, and parse it.

Note, this does not provide any helpful feedback to the client (for example, when an invalid or incomplete json payload is sent, there's no helpful error message like fastapi).

To get slightly developer friendly error messages, such as:

```
curl -v -H "Content-Type: application/json" http://127.0.0.1:8080 -d '{"name": "fred"}'
...
missing field `number` at line 1 column 16(base)
```

Which is slightly more helpful, the `serde_json` create provides the above more useful feedback (though not as good fastapi in combination with Pydantic). TODO: research similar way of getting as good feedback with actix/serde.

See docs: https://actix.rs/docs/request/ "JSON Request"

See also crate `serde_json`.

Clone this repo then

Install:

```
cargo run
```

Then:

```
curl -H "Content-Type: application/json" http://127.0.0.1:8080 -d '{"username": "fred"}'
```
