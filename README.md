# Scientific_Git📲🖱
A Scientific Calculator Built Using Android Studio ☺🤞

# Introduction 
A scientific calculator is a type of electronic calculator, usually but not always handheld, designed to calculate problems in science, engineering, and mathematics. They have completely replaced slide rules in traditional applications, and are widely used in both education and professional settings.
# AIM:
To develop a scientific calculator using Android Studio.

# EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

# ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Perform the Calculator Operation in MainActivity.java

Step 7: Save and run the application.

# PROGRAM:
```
/*
Program to create simple calculator using Android Studio.
Developed by: NITHYAA SRI S S
RegisterNumber: 212222230100
*/

```
# MainActivity.java:
```
package com.example.scientific_calculator;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    Button b1, b2, b3, b4, b5, b6, b7, b8, b9, b0, bdot, bpi, bequal, bmin, bplus, bdiv, bmul, bminus, blog, bac, bc, bb1, bb2, bln, bsin, bcos, btan, binv, bsqrt, bsquare, bfact;
    TextView tvsec, tvmain;
    String pi = "3.14159265";

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        b1 = findViewById(R.id.b1);
        b2 = findViewById(R.id.b2);
        b3 = findViewById(R.id.b3);
        b4 = findViewById(R.id.b4);
        b5 = findViewById(R.id.b5);
        b6 = findViewById(R.id.b6);
        b7 = findViewById(R.id.b7);
        b8 = findViewById(R.id.b8);
        b9 = findViewById(R.id.b9);
        b0 = findViewById(R.id.b0);
        bac = findViewById(R.id.bac);
        bc = findViewById(R.id.bc);
        bb1 = findViewById(R.id.bb1);
        bb2 = findViewById(R.id.bb2);
        bpi = findViewById(R.id.bpi);
        bdot = findViewById(R.id.bdot);
        bequal = findViewById(R.id.bequal);
        bplus = findViewById(R.id.bplus);
        bminus = findViewById(R.id.bminus);
        bmul = findViewById(R.id.bmul);
        bdiv = findViewById(R.id.bdiv);
        binv = findViewById(R.id.binv);
        bsqrt = findViewById(R.id.bsqrt);
        bsquare = findViewById(R.id.bsquare);
        bfact = findViewById(R.id.bfact);
        bln = findViewById(R.id.bln);
        bsin = findViewById(R.id.bsin);
        bcos = findViewById(R.id.bcos);
        btan = findViewById(R.id.btan);
        blog = findViewById(R.id.blog);

        tvmain = findViewById(R.id.tvmain);
        tvsec = findViewById(R.id.tvsec);


        //OnClickListener
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "1");
            }
        });

        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "2");
            }
        });

        b3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "3");
            }
        });

        b4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "4");
            }
        });

        b5.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "5");
            }
        });

        b6.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "6");
            }
        });

        b7.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "7");
            }
        });

        b8.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "8");
            }
        });

        b9.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "9");
            }
        });

        b0.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "0");
            }
        });

        bdot.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + ".");
            }
        });

        bac.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText("");
                tvsec.setText("");
            }
        });

        bc.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String val = tvmain.getText().toString();
                val = val.substring(0, val.length() - 1);
                tvmain.setText(val);
            }
        });

        bplus.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "+");
            }
        });

        bminus.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "-");
            }
        });

        bdiv.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "÷");
            }
        });

        bmul.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "×");
            }
        });

        bsqrt.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String val = tvmain.getText().toString();
                double r = Math.sqrt(Double.parseDouble(val));
                tvmain.setText(String.valueOf(r));
            }
        });


        bb1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "(");
            }
        });

        bb2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + ")");
            }
        });

        bpi.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvsec.setText(bpi.getText());
                tvmain.setText(tvmain.getText() + pi);
            }
        });

        bsin.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "sin");
            }
        });

        bcos.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "cos");
            }
        });

        btan.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "tan");
            }
        });

        binv.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "^" + "(-1)");
            }
        });

        bfact.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int val = Integer.parseInt(tvmain.getText().toString());
                int fact = factorial(val);
                tvmain.setText(String.valueOf(fact));
                tvsec.setText(val + "!");
                Toast toast=Toast.makeText(getApplicationContext(),"The factorial of "+val+" is "+fact ,Toast.LENGTH_LONG);
                toast.show();
            }

        });

        bsquare.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                double d = Double.parseDouble(tvmain.getText().toString());
                double square = d * d;
                tvmain.setText(String.valueOf(square));
                tvsec.setText(d + "²");
                Toast toast=Toast.makeText(getApplicationContext(),"The square of "+d+" is "+square ,Toast.LENGTH_LONG);
                toast.show();

            }
        });

        bln.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "ln");
            }
        });

        blog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                tvmain.setText(tvmain.getText() + "log");
            }
        });

        bequal.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String val = tvmain.getText().toString();
                String replacedstr = val.replace('÷', '/').replace('×', '*');
                double result = eval(replacedstr);
                Toast toast=Toast.makeText(getApplicationContext(),"The result is "+result ,Toast.LENGTH_LONG);
                toast.show();
                tvmain.setText((String.valueOf(result)));
                tvsec.setText(val);

            }
        });

    }

    //Factorial function
    int factorial(int n) {
        return (n == 1 || n == 0) ? 1 : n * factorial(n - 1);
    }

    //eval function
    public static double eval(final String str) {
        return new Object() {
            int pos = -1, ch;

            void nextChar() {
                ch = (++pos < str.length()) ? str.charAt(pos) : -1;
            }

            boolean eat(int charToEat) {
                while (ch == ' ') nextChar();
                if (ch == charToEat) {
                    nextChar();
                    return true;
                }
                return false;
            }

            double parse() {
                nextChar();
                double x = parseExpression();
                if (pos < str.length()) throw new RuntimeException("Unexpected: " + (char) ch);
                return x;
            }

            //Grammer:
            //expression = term | expression '+' term | expression '-' term
            //term = factor | term '*' factor | term '/' factor
            //factor = '+' factor | '-' factor | '(' expression ')'
            //        | number | factorName factor | factor '^' factor

            double parseExpression() {
                double x = parseTerm();
                for (; ; ) {
                    if (eat('+')) x += parseTerm(); //Addition
                    else if (eat('-')) x -= parseTerm(); //Subtraction
                    else return x;
                }
            }

            double parseTerm() {
                double x = parseFactor();
                for (; ; ) {
                    if (eat('*')) x *= parseTerm(); //Multiplication
                    else if (eat('/')) x /= parseTerm(); //Division
                    else return x;
                }
            }

            double parseFactor() {

                if (eat('+')) return parseFactor(); //Unary Plus
                if (eat('-')) return -parseFactor(); //Unary Minus

                double x;
                int startPos = this.pos;
                if (eat('(')) { // Parentheses
                    x = parseExpression();
                    eat(')');
                } else if ((ch >= '0' && ch <= '9') || ch == '.') { //Numbers
                    while ((ch >= '0' && ch <= '9') || ch == '.') nextChar();
                    x = Double.parseDouble(str.substring(startPos, this.pos));
                } else if ((ch >= 'a' && ch <= 'z') || ch == '.') { //Functions
                    while ((ch >= 'a' && ch <= 'z') || ch == '.') nextChar();
                    String func = str.substring(startPos, this.pos);
                    x = parseFactor();
                    if (func.equals("sqrt")) x = Math.sqrt(x);
                    else if (func.equals("sin")) x = Math.sin(Math.toRadians(x));
                    else if (func.equals("cos")) x = Math.cos(Math.toRadians(x));
                    else if (func.equals("tan")) x = Math.tan(Math.toRadians(x));
                    else if (func.equals("log")) x = Math.log10(x);
                    else if (func.equals("ln")) x = Math.log(x);
                    else throw new RuntimeException("Unknown function: " + func);

                } else {
                    throw new RuntimeException("Unexpected: " + (char) ch);
                }
                if (eat('^')) x = Math.pow(x, parseFactor()); //Exponentiation
                return x;
            }

        }.parse();

    }
    }
```
#Activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:weightSum="10"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/tvsec"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:background="@color/black"
        android:text=""
        android:textColor="@color/yellow"
        android:textSize="30sp"
        android:textAlignment="viewEnd"
        android:padding="25dp"
        android:gravity="bottom"
        android:maxLines="1"
        android:layout_weight="2"
        tools:ignore="RtlCompat" />

    <TextView
        android:id="@+id/tvmain"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:background="@color/black"
        android:text=""
        android:textColor="@color/white"
        android:textSize="30sp"
        android:textAlignment="viewEnd"
        android:padding="15dp"
        android:gravity="bottom"
        android:maxLines="1"
        android:layout_weight="1"
        tools:ignore="RtlCompat" />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="7"
        android:orientation="vertical">
        <LinearLayout
            android:orientation="vertical"
            android:weightSum="7"
            android:layout_width="match_parent"
            android:layout_height="match_parent">
            <LinearLayout
                android:orientation="horizontal"
                android:layout_weight="1"
                android:layout_width="match_parent"
                android:layout_height="match_parent">
                <LinearLayout
                    android:orientation="horizontal"
                    android:weightSum="4"
                    android:layout_width="match_parent"
                    android:layout_height="match_parent">
                    <Button
                        android:id="@+id/bac"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="AC"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/bc"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="C"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/bb1"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="("
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/bb2"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text=")"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>

                </LinearLayout>

            </LinearLayout>
            <LinearLayout
                android:orientation="horizontal"
                android:layout_weight="1"
                android:layout_width="match_parent"
                android:layout_height="match_parent">
                <LinearLayout
                    android:orientation="horizontal"
                    android:weightSum="5"
                    android:layout_width="match_parent"
                    android:layout_height="match_parent">
                    <Button
                        android:id="@+id/bsin"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="sin"
                        android:textAllCaps="false"

                        android:textSize="26sp"
                        android:layout_weight="1"
                        android:background="@color/yellow"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/bcos"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="cos"
                        android:textAllCaps="false"
                        android:textSize="26sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/btan"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="tan"
                        android:textAllCaps="false"
                        android:textSize="26sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/blog"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="log"
                        android:textAllCaps="false"
                        android:textSize="26sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/bln"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="ln"
                        android:textAllCaps="false"
                        android:textSize="26sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>

                </LinearLayout>

            </LinearLayout>
            <LinearLayout
                android:orientation="horizontal"
                android:layout_weight="1"
                android:layout_width="match_parent"
                android:layout_height="match_parent">
                <LinearLayout
                    android:orientation="horizontal"
                    android:weightSum="5"
                    android:layout_width="match_parent"
                    android:layout_height="match_parent">
                    <Button
                        android:id="@+id/bfact"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="x!"
                        android:textAllCaps="false"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/bsquare"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="x²"
                        android:textAllCaps="false"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/bsqrt"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="√"
                        android:textAllCaps="false"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/binv"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="1/x"
                        android:textAllCaps="false"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>
                    <Button
                        android:id="@+id/bpi"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="π"
                        android:textAllCaps="false"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>

                </LinearLayout>

            </LinearLayout>
            <LinearLayout
                android:orientation="horizontal"
                android:layout_weight="1"
                android:layout_width="match_parent"
                android:layout_height="match_parent">
                <LinearLayout
                    android:orientation="horizontal"
                    android:weightSum="4"
                    android:layout_width="match_parent"
                    android:layout_height="match_parent">
                    <Button
                        android:id="@+id/b7"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="7"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/b8"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="8"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/b9"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="9"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/bdiv"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="÷"
                        android:textAllCaps="false"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>

                </LinearLayout>

            </LinearLayout>
            <LinearLayout
                android:orientation="horizontal"
                android:layout_weight="1"
                android:layout_width="match_parent"
                android:layout_height="match_parent">
                <LinearLayout
                    android:orientation="horizontal"
                    android:weightSum="4"
                    android:layout_width="match_parent"
                    android:layout_height="match_parent">
                    <Button
                        android:id="@+id/b4"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="4"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/b5"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="5"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/b6"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="6"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/bmul"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="×"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>

                </LinearLayout>

            </LinearLayout>
            <LinearLayout
                android:orientation="horizontal"
                android:layout_weight="1"
                android:layout_width="match_parent"
                android:layout_height="match_parent">
                <LinearLayout
                    android:orientation="horizontal"
                    android:weightSum="4"
                    android:layout_width="match_parent"
                    android:layout_height="match_parent">
                    <Button
                        android:id="@+id/b1"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="1"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/b2"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="2"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/b3"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="3"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/bminus"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="-"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>

                </LinearLayout>

            </LinearLayout>
            <LinearLayout
                android:orientation="horizontal"
                android:layout_weight="1"
                android:layout_width="match_parent"
                android:layout_height="match_parent">
                <LinearLayout
                    android:orientation="horizontal"
                    android:weightSum="4"
                    android:layout_width="match_parent"
                    android:layout_height="match_parent">
                    <Button
                        android:id="@+id/b0"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="0"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/bdot"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="."
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/bequal"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="="
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/white">

                    </Button>
                    <Button
                        android:id="@+id/bplus"
                        android:layout_width="match_parent"
                        android:layout_height="match_parent"
                        android:text="+"
                        android:textSize="30sp"
                        android:layout_weight="1"
                        android:background="@color/black"
                        android:textColor="@color/lime">

                    </Button>

                </LinearLayout>

            </LinearLayout>

        </LinearLayout>

    </LinearLayout>

</LinearLayout>
```
# Android_Manifest.xmL:

```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    package="com.example.scientific_calculator">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.SCIENTIFIC_CALCULATOR"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```
# OUTPUT:
![image](https://github.com/ssnithyaasri/Scientific_Git/assets/119122478/6de1f08c-ebcd-4b49-a007-cfd30540683b)
![image](https://github.com/ssnithyaasri/Scientific_Git/assets/119122478/88530f75-94b8-486e-a222-d01659051f4d)


# Result:
Thus a Simple Android Application for scientific claculator using Android Studio was developed and executed successfully.

