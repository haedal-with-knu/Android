## 기본 위젯들의 특징과 속성

### 텍스트뷰(TextView)


`android:text` : 텍스트뷰의 `text`속성은 표시되는 문자열을 설정한다.
<br>텍스트의 속성을 설정하는 방법은 직접 입력하거나, `/app/res/values/strings.xml` 파일에 작성하는 방법이 있다.

`strings.xml` 파일에 작성하는 방법은 다음과 같다.
```xml
<resources>
    <string name="app_name">widget</string>
    <string name="textview_text">Haedal</string>
</resources>
```
그다음에, 레이아웃 XML 파일에서 텍스트뷰를 추가한 후 `text`속성을 `android:text="@string/textview_text" ` 로 설정해주면 된다.


`android:textColor` : 텍스트뷰의 문자열의 색상을 설정한다. 일반적으로 `##AARRGGBB` 포맷을 사용하며, 4종류의 값은 각각 **Alpha**, **Red**, **Green**, **Blue**를 의미한다.

`android:textSize` : 텍스트뷰의 문자열의 크기를 설정한다. 단위로는 **"dp"**, **"sp"**, **"px"** 을 사용한다.

`android:maxLines` : 텍스트뷰에서 표시하는 문자열의 최대 줄 수를 설정한다.


### 버튼(Button)

버튼은 텍스트뷰를 상속하여 정의되어 있기때문에, `text`, `textColor`, `textSize` 등의 속성을 사용할 수 있다.

`android:onClick` : 버튼을 클릭했을 때 실행되는 메소드를 설정할 수 있다.

### 에디트텍스트(EditText)

에디트텍스트는 입력상자의 역할을 하는 위젯으로, 사용자에게 값을 입력받을 때 사용한다.

`android:hint` : 에디트텍스트에 간단한 안내문을 표시할 수 있다.
 
 `android:inputType` : **number**, **text** 등 입력받을 데이터 형태를 설정할 수 있다.


### 이미지뷰와 이미지 버튼

이미지뷰와 이미지 버튼은 이미지를 화면에 표시할 때 사용한다. 이미지를 나타내려면 `/app/res/drawable` 폴더에 이미지를 저장한 후 속성값으로 정해주면 된다.

`android:src`, `app:srcCompat` : 이미지뷰의 원본 이미지를 설정한다.

`maxWidth`, `maxHeight` : 이미지가 표시되는 최대 폭, 높이를 설정한다.

 
 