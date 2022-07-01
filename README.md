# React helper hook that creates and updates state.

## How to use:

```
import React from 'react';

import { useForm }from './FormHook';

export default const RandomForm = () => {

	const { formState, handleInputChange } = useForm({
		email: "",
		password: "",
	});

	const {email, password} = formState;

	const handleSubmit = (e) => {
		e.preventDefault();
		// Do as you wish :)
	}

	return(
		<form onSubmit={handleSubmit}>
			<input
				type="email"
				name="email"
				value={email}
				onChange={handleInputChange}
			/>
			<input
				type="password"
				name="password"
				value={password}
				onChange={handleInputChange}
			/>
			<button>Submit</button>
		</form>
	)
}
```

# This doesn't only make code reusable (legit the purpose of react) but it also saves a ton of time when it comes to having multiple forms on a page.
