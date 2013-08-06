in the name of god
-----------------

Installation Zarinpal payment modules for persian tomatocart V1.1.1
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

1. upload zarinpal.zip to your server (tomatocart folder) and extract it.

2. line 248 in \includes\modules\order_confirmation_form.php find :


echo '<div style="text-align:left;">' . osc_draw_image_submit_button('button_confirm_order.gif', $osC_Language->get('button_confirm_order'), 'id="btnConfirmOrder"') . '</form></div>'; 


and replace with :


// start change for zarinpal payment modules
  if ($form_action_url == 'https://www.zarinpal.com/users/pay_invoice/') {
  echo '</form>';
  } else {  
  echo '<div style="text-align:left;">' . osc_draw_image_submit_button('button_confirm_order.gif', $osC_Language->get('button_confirm_order'), 'id="btnConfirmOrder"') . '</form></div>';
  }
// end change for zarinpal payment modules 


3. go to administration side of your shop and start -> modules -> payment and active zarinpal modules

-------------------
Ali Masooumi
shahrivar 1390
