Here is a **simple, clear, step-by-step guide** to build your **Blog Website using Maven** from scratch.

---

# 🌐 **Two-Page Blog Website Using Maven – Step-by-Step Guide**

## ✅ **1. Create the Project Structure**

You can do this using Spring Initializr (recommended for beginners).

### **Step 1: Generate Spring Boot Project**

1. Go to: [https://start.spring.io](https://start.spring.io)
2. Choose:

   * **Project:** Maven
   * **Language:** Java
   * **Spring Boot:** 3.x
   * **Dependencies:**

     * Spring Web
   * **Packaging:** Jar
3. Click **Generate**, unzip the folder.

### **Project folder structure looks like:**

```
src/
 ├─ main/
 │   ├─ java/com/example/blog
 │   │     └─ BlogApplication.java
 │   └─ resources/
 │         ├─ static/ (CSS, JS files)
 │         └─ templates/ (HTML files)
pom.xml (Maven file)
```

---

# ✏️ **2. Create the Two HTML Pages**

### **Step 1: In `src/main/resources/templates/` create:**

* **index.html** → homepage
* **post.html** → blog post page

### Example:

**index.html**

```html
<!DOCTYPE html>
<html>
<body>
<h1>My Blog</h1>
<a href="/post">Read Post</a>
</body>
</html>
```

**post.html**

```html
<!DOCTYPE html>
<html>
<body>
<h1>My First Blog Post</h1>
<p>This is my blog content.</p>
</body>
</html>
```

---

# ⚙️ **3. Add Controller to Show Pages**

In `src/main/java/com/example/blog/` create:

### **HomeController.java**

```java
package com.example.blog;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class HomeController {

    @GetMapping("/")
    public String home() {
        return "index";
    }

    @GetMapping("/post")
    public String post() {
        return "post";
    }
}
```

This connects your HTML pages to URL routes.

---

# 🧩 **4. Push Code to GitHub**

### Step-by-step:

1. Create a new repo on GitHub.
2. Open your project folder in CMD.
3. Run:

```
git init
git add .
git commit -m "Initial blog app"
git remote add origin <your-repo-url>
git push -u origin main
```

---

# 🔧 **5. Configure Maven (Already done automatically)**

Maven works through **pom.xml**.
Inside pom.xml, Spring Initializr already added:

* Project metadata
* Dependencies
* Build settings

You don’t need to change anything.

---

# 🚀 **6. Run Maven Commands**

### **1️⃣ Clean previous builds**

```
mvn clean
```

### **2️⃣ Compile code**

```
mvn compile
```

### **3️⃣ Run project**

```
mvn spring-boot:run
```

Now open:
👉 [http://localhost:8080/](http://localhost:8080/)

### **4️⃣ Create a JAR file (deployable build file)**

```
mvn package
```

Generated file becomes ready:

```
target/blog-0.0.1-SNAPSHOT.jar
```

### **Run the build file**

```
java -jar target/blog-0.0.1-SNAPSHOT.jar
```

---

# 🎉 **Done!**

You built a **two-page blog**,
pushed to **GitHub**,
configured **Maven**,
and generated the **deployable JAR**.

---

If you want, I can:
👉 Give complete ready folder structure
👉 Provide full HTML/CSS templates
👉 Help solve "mvn not recognized" error
Just tell me!
