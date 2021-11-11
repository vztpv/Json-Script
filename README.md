# Json-Script

# Example..

    # json -> var
    # json_ptr -> var_ptr 

    var Test = { "int_value" : 345, "test" : { "x" : 567 } };
    var Test2 = ["RUS", "USA"];
    var test = { "RUS" : { "power" : { "army" : 90 } }, "USA" : { "power" : { "army" : 100 } } };
    var int_value = 123;
    var str_value = "wow lost ark";

    var_ptr x = Test{}."int_value";
    var_ptr y = Test2[].0;
    var_ptr z = Test{}."test"{}."x";

    var_ptr a = &int_value;
    var_ptr b = &str_value;

    var c = *a;
    var d = *b;

    var _x = Test{}."int_value".key;
    var _y = Test{}."int_value".value;

    var xx = Test.clone;
    var yy = Test{}."int_value".clone;

    var str_value2 = "RUS";
    var_ptr w = test{}.str_value2{}."power"{}."army";
    # w.value = 100;

    str_value2 = "USA";
    var_ptr ww = test{}.str_value2{}."power"{}."army"

    var i = 0;
    while i < Test2[].size {
      test{}.(Test2[].i.value){}."power"{}."army";	
      i = i + 1;
    }
