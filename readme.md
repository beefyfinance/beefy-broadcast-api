# Description

To improve beefy ecosystem and have a simplify the way to broadcast alarms or messages, we build a modular and flexible API that receive message with specification of how to broadcasting and it.

# Integrations

Current integration and future integrations

- [x] Discord
- [ ] Twitter
- [ ] Telegram

# Enviroment Variables

see [./env.example](env.example) as reference of env variables to use

# Endpoints

## create a message

```js
/**
 * Request
 * POST /broadcasts?apikey="this is secret apikey"
 */
{
	username: 'Messenger Cow', // [optional] default is 'Messenger Cow'
	avatar: 'cow.png', // [optional] default is ./src/images/messenger_cow.png
	type: 'warning', // ( info | warning | error | fatal )
	title: 'subsidy is lower than 10%',
	message: 'be care on this things be cause jessy can do a disaster on the lab without me',
	platforms: ['discord'], // ( discord | telegram | twitter )
}
/**
 * Response
 */
{
	success: true,
	message: 'broadcasting the message my friend'
}
```
