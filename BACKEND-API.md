# API Specification - Galleria

### 1. General Specifications
PROPERTY | VALUE
------------ | -------------
{API-URL} | http://api.example.com/api/v1/


### 2. User Authentication
###### Endpoint
 > POST {API-URL}/login

No ***access_token*** required
 
###### Fields
* id (valid email or telephone number)
* password (min 6 characters)

###### Response Object
* status
	* if **OK**, return a ***user*** object
	* if **FAILED**, return ***error*** field with error description
	
```javascript
{
	status: OK,
	user: {
		...user object here...	
	}
}

```


### 3. User Registration
###### Endpoint
 > POST {API-URL}/register
 
###### Fields
* names
* telephone
* email
* password

###### Response Object
* status
	* if **OK**, return a ***user*** and ***access_token*** object
	* if **FAILED**, return ***error*** field with error description
	
```javascript
{
	status: OK,
	user: {
		...user object here...	
	},
	token: 0edb90ed35e7e8d9669f0b0a07244bc7
}

```
