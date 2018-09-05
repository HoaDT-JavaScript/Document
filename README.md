# Document

# String 
==Hàm format số: thêm dấu phẩy vào đơn vị nghìn và làm tròn đến n số sau dấu phẩy
console.log(formatNumber("0.156"));

function formatNumber(str, n) {
    str = Number(str).toFixed(n);
    var len = str.length;
    var s = "";
    var count = str.indexOf(".");
    var i = count - 1;
    while (i >= 0) {
        s = s + str[count - 1 - i];
        if (i % 3 == 0 && i != count - 1 && i != 0) s = s + ",";
        i--;
    }
    for (i = count; i < len; i++)
        s = s + str[i];
    return s;
}
