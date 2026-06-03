Cambiar la linea 16:
-CMD ["sh", "-c", "tail -f /dev/null"]
Por este comando:
-CMD ["npm", "test"]
Ya que de lo contrario me toco entrar manualmente al contenedor de la soguiente manera 
-docker exec -it cityfix_container sh
-npm test

Pruebas con la correción del comando de arranque:
 ✔ Container cityfix_container Recreated                                                                               0.6s
Attaching to cityfix_container

cityfix_container  | > cityfix-app@1.0.0 test
cityfix_container  | > jest                                                                                                
cityfix_container  |                                                                                                       
 PASS  src/utils/reportEngine.test.js
  Pruebas de Red E2E Live Network - CityFix
    ✓ 1. Debería conectar exitosamente y devolver un array auténtico de JavaScript (1457 ms)                               
    ✓ 2. Debería certificar que la longitud del array es mayor a cero (lee datos inyectados) (122 ms)                      
    ✓ 3. Debería certificar que el primer registro tenga las propiedades estructuradas correctamente (119 ms)              
cityfix_container  |
Test Suites: 1 passed, 1 total                                                                                             
cityfix_container  | Tests:       3 passed, 3 total                                                                        
cityfix_container  | Snapshots:   0 total
cityfix_container  | Time:        2.874 s
cityfix_container  | Ran all test suites.                                                                                  

cityfix_container exited with code 0
PS C:\Users\245G8-R5\OneDrive - SENA\Escritorio\prueba-3\CityFixAppDanilo> 

v View in Docker Desktop   o View Config   w Enable Watch   d Detach