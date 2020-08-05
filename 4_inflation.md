### 레이아웃 인플레이션

인플레이션(Inflation) : XML 레이아웃의 내용을 메모리 상에 객체화하고 화면에 보여주는 과정.

아래 코드는 안드로이드 스튜디오에서 새 프로젝트를 만들게 되면 생성되는 `MainActivity.java`의 코드이다.
```java
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
```

`setContentView(...)` : View를 메모리에 객체화 하고 화면 전체에 나타낸다.

`setContentView` 메소드는 화면 전체를 설정하는 역할만 하기 때문에, 부분 화면을 메모리에 객체화 할수 없다.
<br> -> 부분 화면을 인플레이션 하기 위해 안드로이드에서 제공하는 `LayoutInflater` 클래스 사용해야 한다.


```java
LinearLayout container = (LinearLayout) findViewById(R.id.container);

LayoutInflater inflater = (LayoutInflater)getSystemService(Context.LAYOUT_INFLATER_SERVICE);
inflater.inflate(R.layout.sub, container, true);
``` 
getSystemService() 메소드를 통해 참조할 수 있다.

`inflater.inflate(객체화 시킬 xml, 부모 컨테이너, true:바로 inflation)`

```java
//예제 추가
```


### 화면 간 전환하기

Activity를 소스 코드에서 띄울 때는 startActivity() 메소드를 사용.
하지만 앱을 사용하다 보면 여러 화면을 띄워서 활동한 후 화면을 닫고 메인화면으로 돌아올 때 결과를 받아 사용해야 하는 일이 많다.
Activity로부터 결과를 받고 처리하기 위해서는 startActivityForResult() 메소드를 사용해야한다.


```java
startActivityForResult(intent intent, int requestCode)
```

```
setResult(RESULT_OK, intent)
```
```java
onActivityResult(int requestCode, int resultCode, Intent intent)
```

`인텐트(Intent)`: 메시징 객체로 컴포넌트 간에 호출 및 데이터 전달 https://developer.android.com/guide/components/intents-filters?hl=ko
```java

   //예제

```

### 액티비티의 생명 주기(Life Cycle)

