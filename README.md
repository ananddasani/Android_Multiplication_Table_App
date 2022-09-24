# Multiplication_Table_App
An App to Remember Multiplication Tables 😁

This topic is a part of [My Complete Andorid Course](https://github.com/ananddasani/Android_Apps)

# Code

#### 1st Activity 
```
TextView textView;
SeekBar seekBar;
ListView listView;

textView = findViewById(R.id.textView);
listView = findViewById(R.id.listView);
seekBar = findViewById(R.id.seekBar);

        seekBar.setMax(20);
        
        seekBar.setOnSeekBarChangeListener(new SeekBar.OnSeekBarChangeListener() {
            @Override
            public void onProgressChanged(SeekBar seekBar, int progress, boolean fromUser) {
//                Toast.makeText(getApplicationContext(), "Calculated Table of " + progress, Toast.LENGTH_SHORT).show();
                calculateTable(progress);
            }

            @Override
            public void onStartTrackingTouch(SeekBar seekBar) {

            }

            @Override
            public void onStopTrackingTouch(SeekBar seekBar) {

            }
        });
    }
    
    public void calculateTable(int tableOf) {
        ArrayList<String> arrayList = new ArrayList<>();

        for (int i = 1; i <= 10; i++)
            arrayList.add(tableOf + " X " + i + " = " + (tableOf * i));

        ArrayAdapter<String> arrayAdapter = new ArrayAdapter<>(getApplicationContext(), android.R.layout.simple_list_item_1, arrayList);
        listView.setAdapter(arrayAdapter);

        textView.setText("Multiplication Table of " + tableOf);
    }
        
```

# App Highlight

![Multiplication Table App1](https://user-images.githubusercontent.com/74413402/192092935-ddba9770-37c6-4d1c-86d7-c0d5f3823cae.png)
![Multiplication Table App2](https://user-images.githubusercontent.com/74413402/192092941-e0ee64f2-8c04-4a2e-bd6d-abe3fdabe291.png)
![Multiplication Table Code](https://user-images.githubusercontent.com/74413402/192092943-59c66cf1-5f4e-470b-9ac5-203b395f0e09.png)
