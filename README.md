
### Zależności

`plugins {
kotlin("plugin,serialization") version "X"
}`

`implementation("org.jetbrains.kotlinx:kotlinx-serialization-json.X")`

### Serializacja
Serializacja to proces zamiany obiektów programu na format zgodny z danymi systemu lub bazy danych. Deserializacja jest odwórceniem tego procesu.

Rodzaje bibliotek kotlinx.serialization:
- json
- ProtocolBuffers
- CBOR
- Properties
- HOCON

### Serializacja z DC na json:

* oznacz DC adnotacją `@Serializable`

`val toJson = Json.encodeToString(DC)`

Jeśli pola DC mają domyślne wartości to: `val toJson = Json.{ encodeDefaults = true }.encodeToString(DC)`


### Deserializacja z json na DC:

`val fromJson = Json.decodeFromString(<DC>(toJson))`
