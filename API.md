
### new Team(options)


#### work


#### attend(note)


#### regroup(options)


### new Events()

Creates an events emitter via an async iterator interface.

Example:

```js
const Teamwork = require('@hapi/teamwork');

const handler = async function() {

  const events = new Teamwork.Events();
  
  events.emit(1);
  events.emit(2);
  events.end();
  
  const items = [];
  
  for await (const item of events.iterator()) {
      items.push(item);
  }

  return items //Returns [1, 2, 3];
}
```

#### iterator()


#### emit(value)


#### end()

