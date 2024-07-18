## 中文文档
---
### 简介

`LocalStorage` 是一个简单的本地存储类，用于在文件系统中存储和检索数据。它支持基本的键值对存储，并提供了一些额外的功能，如设置过期时间。


### 下载

你可以通过以下链接下载我们的最新发布版本：

- [下载最新发布版本](https://github.com/StrGin/zeppos1.0-localstorage/releases/tag/re)
  
### 初始化

首先，你需要初始化 `LocalStorage` 实例：

```javascript
import { LocalStorage } from './LocalStorage';

const storage = new LocalStorage('local_storage.txt');
```

### 设置数据

你可以使用 `setItem` 方法来存储数据：

```javascript
storage.setItem('name', 'Alice');
storage.setItem('age', 30);
```

### 获取数据

使用 `getItem` 方法来检索数据：

```javascript
const name = storage.getItem('name');
const age = storage.getItem('age');

console.log(name); // 输出: Alice
console.log(age);  // 输出: 30
```

### 删除数据

使用 `removeItem` 方法来删除数据：

```javascript
storage.removeItem('name');
```

### 清除所有数据

使用 `clear` 方法来清除所有存储的数据：

```javascript
storage.clear();
```

### 设置带过期时间的数据

你可以使用 `setItemWithExpiry` 方法来存储带有过期时间的数据：

```javascript
storage.setItemWithExpiry('token', 'abc123', 3600000); // 1小时后过期
```

### 获取带过期时间的数据

使用 `getItemWithExpiry` 方法来检索带有过期时间的数据：

```javascript
const token = storage.getItemWithExpiry('token');

if (token) {
  console.log('Token is valid:', token);
} else {
  console.log('Token has expired or does not exist');
}
```

---

