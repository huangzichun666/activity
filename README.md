# activity
Android实验一

实验activity跳转界面:


![](https://raw.githubusercontent.com/huangzichun666/activity/master/Image/%60R0VCR41E@X%7D79C3ZV6ZH8D.png)


实验结果截图：


![](https://raw.githubusercontent.com/huangzichun666/activity/master/Image/CP1WQ81%7DD3B1JFETVPSVEKO.png)


实验activity代码：
public class MainActivity extends AppCompatActivity {

    Button button;
    private String TAG="MainActivity";
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.d(TAG, "onCreate");
        init();
        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent = new Intent(MainActivity.this, SecondActivity.class);
                startActivity(intent);
            }
        });
    }

    public void init(){
        button = findViewById(R.id.button);
    }
    @Override
    protected void onStart() {
        super.onStart();
        Log.d(TAG, "onStart");
    }

    @Override
    protected void onResume() {
        super.onResume();
        Log.d(TAG, "onResume");
    }

    @Override
    protected void onPause() {
        super.onPause();
        Log.d(TAG, "onPause");
    }

    @Override
    protected void onStop() {
        super.onStop();
        Log.d(TAG, "onStop");
    }

    @Override
    protected void onRestart() {
        super.onRestart();
        Log.d(TAG, "onRestart");
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();
        Log.d(TAG, "onDestroy");
    }
}

