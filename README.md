# OptionMenuOnActivity

- R.menu.menu
```xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">

    <item android:id="@+id/menu1" android:title="Menu 1"/>
    <item android:id="@+id/menu2" android:title="Menu 2 Switch Fragment"/>
</menu>
```

- MainActivity.java
```java
public class MainActivity extends AppCompatActivity {

    ...

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.menu, menu);
        return super.onCreateOptionsMenu(menu);
    }

    @Override
    public boolean onOptionsItemSelected(@NonNull MenuItem item) {
        int id = item.getItemId();

        switch (id){
            case R.id.menu1:
                Toast.makeText(getApplicationContext(), "Menu 1", Toast.LENGTH_SHORT).show();
                return true;
            case R.id.menu2:
                Toast.makeText(getApplicationContext(), "Menu 2", Toast.LENGTH_SHORT).show();
                return true;
        }
        return super.onOptionsItemSelected(item);
    }
}
```

---

```
Copyright 2022 M. Fadli Zein
```


