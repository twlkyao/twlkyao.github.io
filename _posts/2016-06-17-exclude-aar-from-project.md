---
layout: default
title: exclude-aar-from-project（排除特定aar）
---

# {{page.title}}

When you are using Android Studio to build your project, since it use maven depedences, you may encounter that some aars contains different base aars, and you want to exclude them, you can add lines in your build.gradle file as follows:  

```gradle
configurations {  
    all*.exclude group: 'your-group_id', module: 'your-artifact_id'  
}  
```

In Chinese:  
当你使用Android Studio构建你的Android工程的时候，可能会遇到由于使用多个aar，然后aar又使用不同版本的底层的库导致的不一致，这时可以在build.gradle中添加类似下边的代码将你不想使用的库排除出去  

```gradle
configurations {  
    all*.exclude group: 'your-group_id', module: 'your-artifact_id'  
}  
```

<p>{{ page.date | date_to_string }}</p>
