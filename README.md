# 2.1

FullAdder.hdl
CHIP FullAdder {
    IN a, b, c;  // 1-bit inputs
    OUT sum,     // Right bit of a + b + c
        carry;   // Left bit of a + b + c

    PARTS:
    HalfAdder(a=a, b=b, sum=w1, carry=c1);
    HalfAdder(a=w1, b=c, sum=sum, carry=c2);
    Or(a=c1, b=c2, out=carry);
}

![image](https://github.com/user-attachments/assets/85166d71-6c00-4a0a-baa1-5b5eaad01575)

HalfAdder.hdl

