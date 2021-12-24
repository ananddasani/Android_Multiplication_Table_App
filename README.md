# Multiplication_Table_App
An App to Remember Multiplication Tables 😁

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

<img src="app_images/Multiplication Table Code.png" width="1000" /><br>

<img src="app_images/Multiplication Table App1.png" width="300" /><br>

<img src="app_images/Multiplication Table App2.png" width="300" /><br>
