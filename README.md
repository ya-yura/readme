# Erston: Onboarding and Documentation  

Welcome to **Erston** – a programming language designed specifically for the Cleverence platform. This guide will help you quickly master Erston's syntax, set up your development environment, and build your first application.  

---

## 📌 Introduction  
Erston is built for developing business applications on the Cleverence platform. It combines the rigor of a strongly typed language with the convenience of declarative UI design.  

---

## 🚀 Installation and Setup  
Before you start, install the Erston SDK.  

### 1. Installing Erstudio (GUI)  
Erstudio is the official IDE for Erston. To install it:  
```sh  
curl -L -o erstudio_installer.sh https://cleverence.com/download/erstudio  
chmod +x erstudio_installer.sh  
./erstudio_installer.sh  
```  

### 2. Installing the CLI Compiler  
For terminal-based workflows, install the CLI version:  
```sh  
curl -L -o erston-cli https://cleverence.com/download/erston-cli  
chmod +x erston-cli  
mv erston-cli /usr/local/bin/erston  
```  

---

## ✍️ Syntax Basics  

### Variables and Types  
Erston uses strict typing:  
```erston  
let a: int = 42;  
let b: string = "Hello, world!";  
let c: bool = true;  
```  

### Functions  
```erston  
func sum(a: int, b: int) -> int {  
    return a + b;  
}  
```  

---

## 🔌 Working with the Cleverence Platform  

### Connecting to APIs  
```erston  
let response = http.get("https://api.cleverence.com/data");  
if response.status == 200 {  
    log(response.body);  
}  
```  

---

## 📊 Database Operations  
Erston includes a built-in ORM:  
```erston  
let users = db.query<User>().where(u -> u.age > 18).toList();  
```  

---

## 🎨 Building UIs  
Design declarative interfaces with ease:  
```erston  
ui {  
    button "Click me" {  
        on click {  
            log("Button clicked!");  
        }  
    }  
}  
```  

---

## ⚠️ Error Handling  
```erston  
try {  
    let data = api.fetch("/data");  
} on fail {  
    log("Failed to load data");  
}  
```  

---

## 🛠 Practical Example  
Let’s build a simple app to fetch a product list and display it in a table:  
```erston  
ui {  
    table {  
        columns: ["Name", "Price"]  
        rows: db.query<Product>().toList();  
    }  
}  
```  

---

## 🎯 Conclusion  
You’ve mastered the basics of Erston! Explore the full documentation to build complex applications on the Cleverence platform.  

---  
**Next Steps:**  
- Dive into the [Erston API reference](#) for advanced features.  
- Join the [community forum](#) for support and best practices.  
- Start building your first production-ready app!  

Happy coding! 😊  
```
