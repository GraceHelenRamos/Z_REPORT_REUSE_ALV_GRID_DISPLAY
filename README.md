Na chamada da função os valores informados em hardcode são referencia a performs, onde vc faz a declaração na função e da ação dentro do perform
como nos exemplos F_SET_STATUS e F_USER_COMMAND (acações do usuário)


 CALL FUNCTION 'REUSE_ALV_GRID_DISPLAY' 
    EXPORTING 
      i_callback_program       = sy-repid 
      i_callback_pf_status_set = 'F_SET_STATUS' 
      i_callback_user_command  = 'F_USER_COMMAND' 
      is_layout                = wa_layout 
      it_fieldcat              = it_field_cat[] 
      i_save                   = 'A' 
    TABLES 
      t_outtab                 = pt_alv_log 
    EXCEPTIONS 
      program_error            = 1 
      OTHERS                   = 2. 
  IF sy-subrc <> 0. 
    MESSAGE ID sy-msgid TYPE sy-msgty NUMBER sy-msgno 
               WITH sy-msgv1 sy-msgv2 sy-msgv3 sy-msgv4. 
 
  ENDIF. 


<img width="588" height="233" alt="image" src="https://github.com/user-attachments/assets/8a4b5d91-baef-43f5-94cf-e4527eb3b8e0" />

botão de e-mail criado no PF STATUS, faça a declaração dele -> ENTER -> Defina nome e demais valores-> SALVAR.
<img width="845" height="562" alt="image" src="https://github.com/user-attachments/assets/ac0747ea-ecb8-4c57-86b4-745f6f09a1d4" />
<img width="741" height="490" alt="image" src="https://github.com/user-attachments/assets/205f19e4-2516-4351-ab83-bc73729f4a70" />




 
