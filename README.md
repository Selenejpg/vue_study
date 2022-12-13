Vue's templating syntax: run JavaScript expressions directly in the template.

V-Model permette di tenere d'occhio automaticamente i cambiamenti senza utilizzare degli event listener. I cambiamenti sono automaticamente percepiti da vue cosicchè il testo si aggiorna automaticamente in base al valore inserito nell'input
```
<h1> {{msg}} </h1>
<input v-model="msg" type="text" />
```
All'interno dei baffi è possibile aggiungere metodi JS. Per rendere tutto maiuscolo, infatti basta aggiungere .toLocaleUpperCase()
```
<h1> {{msg.toLocaleUpperCase()}} </h1>
```

All'interno dei baffi è possibile valutare una sola espressione alla volta, se si aggiungono due espressioni si va incontro ad un parsing error, unexpected token. Non è inoltre possibile dichiarare nuove variabili e aggiungere condizioni if o simili (evaluating statements). E' possibile invece aggiungere ternari, anche accorciati grazie all'operatore or

es ternario
```
<h1> {{msg ? msg : 'Welcome'}} </h1>
```

es ternario abbreviato
```
<h1> {{msg || 'Welcome'}} </h1>
```