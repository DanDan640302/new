SELECT *
  FROM tabela
  INTO TABLE @DATA(lt_dados)

  CALL METHOD cl_gui_frontend_services=>gui_dowload
    EXPORTING
      filename  = 'Caminho'.
      filetype   = 'ASC'.
    CHANGING
      data_tab   = lt_dados
