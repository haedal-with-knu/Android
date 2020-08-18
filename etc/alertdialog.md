### AlertDialog 이용하여 입력창 띄우기


```java

final AlertDialog.Builder alertDialog = new AlertDialog.Builder(getContext());

alertDialog.setTitle("제목");
alertDialog.setMessage("메세지");

final EditText editText = new EditText(getContext());
alertDialog.setView(editText);

alertDialog.setPositiveButton("YES", new DialogInterface.OnClickListener() {
    @Override
    public void onClick(DialogInterface dialogInterface, int i) {
        String value = editText.getText().toString();
        dialogInterface.dismiss();
    }
});
alertDialog.setNegativeButton("NO", new DialogInterface.OnClickListener() {
    @Override
    public void onClick(DialogInterface dialogInterface, int i) {
        dialogInterface.dismiss();
    }
});

alertDialog.show();

```