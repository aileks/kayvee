# Kayvee

## Plan Outline

- [ ] Scaffold: `src/`, `include/`, `tests/`, `Makefile`
- [ ] Define `Database`, `Entry`, and ownership rules
- [ ] Start with dynamic array + linear lookup
- [ ] Implement core database operations
- [ ] REPL: read command → parse → execute → respond
- [ ] Implement `SET`, `GET`, `DEL`, `EXISTS`, `KEYS`
- [ ] Tests for parser + database operations
- [ ] Run ASan and fix leaks / invalid memory access
- [ ] Replace linear lookup with a hash table
- [ ] Add automatic hash table resizing
- [ ] Persistence: `SAVE` + load on startup
- [ ] Benchmark, profile, and improve data layout

## Feature Goals

### Core

- [ ] In-memory key/value storage
- [ ] `SET key value`
- [ ] `GET key`
- [ ] `DEL key`
- [ ] `EXISTS key`
- [ ] `KEYS`
- [ ] REPL mode
- [ ] Clear error responses

### Storage

- [ ] Dynamic array backend
- [ ] Linear key lookup
- [ ] Replace dynamic array lookup with hash table
- [ ] Collision handling
- [ ] Automatic resizing
- [ ] Explicit ownership / lifetime rules
- [ ] Clean shutdown; free all memory

### Persistence

- [ ] `SAVE`
- [ ] Load database on startup
- [ ] Simple custom file format
- [ ] Handle malformed / invalid database files safely

### Quality

- [ ] Parser tests
- [ ] Database tests
- [ ] Storage tests
- [ ] Persistence tests
- [ ] Compiler warnings enabled
- [ ] AddressSanitizer-clean
- [ ] No memory leaks
- [ ] Useful logging
- [ ] Benchmark and profile before optimizing

### Stretch

#### Commands

- [ ] `INCR`
- [ ] `DECR`
- [ ] `APPEND`
- [ ] `TTL`
- [ ] `EXPIRE`

#### Tooling

- [ ] Basic benchmark tool
- [ ] Config file
- [ ] CLI flags

#### Networking

- [ ] TCP server
- [ ] Configurable port
- [ ] One client at a time
- [ ] RESP2 command parsing
- [ ] RESP2 responses
- [ ] Basic `redis-cli` compatibility
- [ ] Multiple clients
- [ ] I/O multiplexing with `poll`
