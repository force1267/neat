# [neat](neat.github.io)
write firebase apps in HTML using svelte !

---

## What is it like ?

```HTML
<Firebase config={ APP_CONFIG } hosting auth firestore database storage bind:app on:load=start()>
    <span slot="loading">
        <Loading/>
    </span>
    <span>
        firebase is loaded
    </span>
</Firebase>
```
##### * Loading is some other module
##### * get your APP_CONFIG from your [console](https:console.firebase.google.com)
#### you just loaded firebase scripts !

## Lets authenticate some users

```HTML
<Button text="login using google">
    <Auth google popup bind:user on:success="start(event)"/>
</Button>
```
##### * Button is some other module


## Write to DB with HTML ?!?!?

```HTML
<Button text="get data !">
    <Database write="..realtime database query.." sync bind:info />
    <Firestore write="..firestore query.." info={myinfo}>
        <span slot="error">there was some error<span>
    </Firestore>
    <Firestore read="..another query.." sync bind:info=hisinfo on:success="parse(event)">
        we got {hisinfo} !
    </Firestore>
</Button>
```

### making an app by only using db and auth is possible ! but with storage ...

### Upload a file
