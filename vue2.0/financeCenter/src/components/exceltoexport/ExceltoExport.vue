<template>
    <div>
    </div>
</template>

<script>
    export default {
        mounted(){
            $(function(){
                !function(e){"use strict";var t=function(){function e(e,t,n){t=t||"",n=n||512;var o,r=window.atob(e),i=[];for(o=0;o<r.length;o+=n){var c,a=r.slice(o,o+n),l=Array(a.length);for(c=0;c<a.length;c+=1)l[c]=a.charCodeAt(c);var s=new window.Uint8Array(l);i.push(s)}var x=new window.Blob(i,{type:t});return x}function t(t,n,o,r){var i;if(window.navigator.msSaveBlob)return i=e(n,o),window.navigator.msSaveBlob(i,r),!1;if(window.URL.createObjectURL){i=e(n,o);var c=window.URL.createObjectURL(i);t.href=c}else{var a="data:"+o+";base64,"+n;t.download=r,t.href=a}return!0}var n="2.0.3",o={excel:'<html xmlns:o="urn:schemas-microsoft-com:office:office" xmlns:x="urn:schemas-microsoft-com:office:excel" xmlns="http://www.w3.org/TR/REC-html40"><head><meta name=ProgId content=Excel.Sheet> <meta name=Generator content="Microsoft Excel 11"><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"><!--[if gte mso 9]><xml><x:ExcelWorkbook><x:ExcelWorksheets><x:ExcelWorksheet><x:Name>{worksheet}</x:Name><x:WorksheetOptions><x:DisplayGridlines/></x:WorksheetOptions></x:ExcelWorksheet></x:ExcelWorksheets></x:ExcelWorkbook></xml><![endif]--></head><body><table>{table}</table></body></html>'},r=",",i="\r\n",c=function(e){return window.btoa(window.unescape(encodeURIComponent(e)))},a=function(e,t){return e.replace(RegExp("{(\\w+)}","g"),function(e,n){return t[n]})},l=function(e){return e.nodeType?e:document.getElementById(e)},s=function(e){var t=e,n=-1!==e.indexOf(r)||-1!==e.indexOf("\r")||-1!==e.indexOf("\n"),o=-1!==e.indexOf('"');return o&&(t=t.replace(/"/g,'""')),(n||o)&&(t='"'+t+'"'),t},x=function(e){var t,n,o,c,a="";for(t=0;t<e.rows.length;t+=1){for(o=e.rows[t],n=0;n<o.cells.length;n+=1)c=o.cells[n],a=a+(n?r:"")+s(c.textContent.trim());a+=i}return a},f={version:function(){return n},excel:function(e,n,r){n=l(n);var i={worksheet:r||"Worksheet",table:n.innerHTML},s=c(a(o.excel,i));return t(e,s,"application/vnd.ms-excel","export.xls")},csv:function(e,n,o,a){void 0!==o&&o&&(r=o),void 0!==a&&a&&(i=a),n=l(n);var s="\ufeff"+x(n),f=c(s);return t(e,f,"application/csv","export.csv")}};return f}();"function"==typeof define&&define.amd?define(function(){return t}):"undefined"!=typeof exports?("undefined"!=typeof module&&module.exports&&(exports=module.exports=t),exports.ExcellentExport=t):e.ExcellentExport=t}(this);
            })
        }
    }
</script>