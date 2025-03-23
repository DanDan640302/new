SELECT *
  FROM tabela
  INTO TABLE @DATA(lt_dados)

  CALL METHOD cl_gui_frontend_services=>gui_dowload
    EXPORTING
      filenmane  = 'Caminho'.
      filetype   = 'ASC'.
    CHANGING
      data_tab   = lt_dados
