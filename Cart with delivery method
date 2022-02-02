<script>

$(document).ready(function(){
    
//Добавляем классы для скрытия к нужным пунктам
$(".t706 .t-input-group_in").addClass("adress notshow");
var deliveryRadio = $('[name="delivery"]');
var deliveryHideBlock = $('[data-input-lid="1596750160109"],[data-input-lid="1596750409031"],.adress.notshow');
var citySelect = $('[name="location"]');
var cityRadioButtons = $('[name="cashdelivery"]');
var firstCityOption = $('[name="cashdelivery"]').eq(0).val();

// Hide radio buttons
$('div[data-input-lid="1596750201119"]').hide();

var deliveryViewMethod = deliveryRadio.val() === "Доставка курьером" ? "show" : "hide";

deliveryHideBlock[deliveryViewMethod]();

function onCityChange(e) {
    var value = e.target.value;
    var radio = $('[name="cashdelivery"][value^="' + value.trim() + '"]');
    var addressViewMethod = firstCityOption === value ? "hide" : "show";
    var isAddressRequired = firstCityOption !== value;
    var addressFields = $(".adress.notshow");
    
    addressFields[addressViewMethod]();
    addressFields.find('input').data('tilda-req', +isAddressRequired);
    
    radio.eq(0).prop("checked", true).change();
}

citySelect.on('change', onCityChange);

function onDeliveryChange(e) {
    var value = e.target.value;
    var deliveryViewMethod = value === "Доставка курьером" ? "show" : "hide";
    
    deliveryHideBlock[deliveryViewMethod]();
    deliveryHideBlock.find('select').find('option').eq(0).prop('selected', 'selected').change();
    deliveryHideBlock.find('select').change();
}

deliveryRadio.click(onDeliveryChange);
    
//Функция скрытия всех блоков
function darkside(){
    $(".notshow").css("display" , "none");
};
 
});
</script>
