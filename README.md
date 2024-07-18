# zeppos1.0-localstorage
`LocalStorage` is a simple local storage class for storing and retrieving data in the file system. It supports basic key-value storage and provides additional features such as setting expiration time.

---
[查看中文文档](README_zh.md)

### Download

You can download our latest release version via the following link:

[Download Latest Release]([https://github.com/yourusername/yourrepository/releases/latest/download/yourfile.zip](https://github.com/StrGin/zeppos1.0-localstorage/releases/tag/re))
  
### Initialization

First, you need to initialize the `LocalStorage` instance:

```javascript
import { LocalStorage } from './LocalStorage';

const storage = new LocalStorage('local_storage.txt');
```

### Setting Data

You can use the `setItem` method to store data:

```javascript
storage.setItem('name', 'Alice');
storage.setItem('age', 30);
```

### Getting Data

Use the `getItem` method to retrieve data:

```javascript
const name = storage.getItem('name');
const age = storage.getItem('age');

console.log(name); // Output: Alice
console.log(age);  // Output: 30
```

### Removing Data

Use the `removeItem` method to delete data:

```javascript
storage.removeItem('name');
```

### Clearing All Data

Use the `clear` method to clear all stored data:

```javascript
storage.clear();
```

### Setting Data with Expiry

You can use the `setItemWithExpiry` method to store data with an expiration time:

```javascript
storage.setItemWithExpiry('token', 'abc123', 3600000); // Expires in 1 hour
```

### Getting Data with Expiry

Use the `getItemWithExpiry` method to retrieve data with an expiration time:

```javascript
const token = storage.getItemWithExpiry('token');

if (token) {
  console.log('Token is valid:', token);
} else {
  console.log('Token has expired or does not exist');
}
```

---
