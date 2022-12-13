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

Reactive reference
Per non creare elementi statici si usano delle reactive reference che permettono di manipolare, aggiungere e rimuovere oggetti in modo dinamico. Nel nostro progetto abbiamo dichiarato la variabile items. Abbiamo assegnato una reactive reference grazie a ref(). All'interno vi è un array di tutti i nostri oggetti. Dopodichè abbiamo creato un v-for per creare un loop degli oggetti. Quando dichiariamo un v-for deve sempre essere presente la key che si associa ad ogni elemento ciclato dal v-for. Non è sempre obbligatorio, ma è good practice inserirla sempre. All'interno della variabile dichiarato un id per ogni oggetto all'interno della reactive reference. Una delle cose positive di Vue è che si aggiorna automaticamente. Se rimuovessimo un elemento dalla lista, vue percepisce il cambiamento e lo rimuoverebbe automaticamente