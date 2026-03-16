C4Context
      title Diagrama de Contexto (Nível 1) - BarberPoint

      Person(cliente, "Cliente", "Usuário que deseja agendar serviços na barbearia.")
      Person(admin, "Administrador", "Gerencia os barbeiros, serviços e visualiza os agendamentos.")
      
      System(barberpoint, "BarberPoint", "Plataforma de gerenciamento de barbearias que permite agendamento de serviços e administração do estabelecimento.")

      BiRel(cliente, barberpoint, "Acessa para agendar horários e serviços")
      BiRel(admin, barberpoint, "Acessa para gerenciar barbeiros e agendamentos")

      %% Customização de Estilos
      UpdateElementStyle(barberpoint, $fontColor="white", $bgColor="#1168bd", $borderColor="#0b4884")
      
      %% Customização de Setas
      UpdateRelStyle(cliente, barberpoint, $textColor="blue", $lineColor="blue", $offsetX="10")
      UpdateRelStyle(admin, barberpoint, $textColor="blue", $lineColor="blue", $offsetX="-10")

      %% Configuração de Layout
      UpdateLayoutConfig($c4ShapeInRow="2", $c4BoundaryInRow="1")