# GLSL-ATAN2-DOC
Documentation for ATAN2 in GLSL because the GLSL docs suck.

![image](https://user-images.githubusercontent.com/7478702/196066423-a2ebcd8e-3727-4b43-a934-9ecbd3e6f13c.png)

Above is the implementation output for atan2 or GLSL's `atan(y,x)` function.

The range here in degrees is `0 to pi (0-180 degrees)` and `-pi to 0 (181 to 359 degrees`.

This can be converted to proper radians `0 to 2pi` using the following function:

```GLSL
float atan2(float y, float x) {
    const float PI2 = 6.2831853071795864769252867665590;
    return mod(atan(y,x) + (PI2*0.5), PI2);
}
```
