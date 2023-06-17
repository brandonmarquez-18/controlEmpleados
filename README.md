package cotroldeempleados;
import java.io.InputStream;//LEER DATOS
import java.util.Scanner;//PARA UTILIZAR LA CLASE "Scanner"
import javax.swing.JOptionPane;
import javax.swing.JPanel;
/**
 *
 * @author Sammy Guergachi <sguergachi at gmail.com>
 */
public class CotroldeEmpleados {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
    
        //Pedir # de Empleados
        String num = JOptionPane.showInputDialog("Digita el número de trabajadores a ingresar: ");
        //Conversión
        int numTra = Integer.parseInt(num);
        
        //Arrays
        String [] nombres = new String[numTra];
        String [] direcciones = new String[numTra];
        String [] areas = new String[numTra];
        int [] horasSemana = new int[numTra];
        int [] pagoHora = new int[numTra];
        int [] pagoSemana = new int [numTra];
        
        //Ciclos
        for(int i=0;i<numTra;i++){
            nombres[i] = JOptionPane.showInputDialog("Nombre del empleado #" + (i+1) + ": ");
            direcciones[i] = JOptionPane.showInputDialog("Dirección del empleado #" + (i+1) + ": ");
            areas[i] = JOptionPane.showInputDialog("Área del empleado #" + (i+1) + ": ");
            horasSemana[i] = Integer.parseInt(JOptionPane.showInputDialog("Horas por semana del empleado #" + (i+1) + ": "));
            pagoHora[i] = Integer.parseInt(JOptionPane.showInputDialog("Pago por hora del empleado #" + (i+1) + ": "));
            
            pagoSemana[i] = horasSemana[i] * pagoHora[i];
        }
        for(int i=0;i<numTra;i++){
            JOptionPane.showMessageDialog(null, "Este es el nombre que ingresó del empleado #" + (i+1) + ": " + nombres[i]);
            JOptionPane.showMessageDialog(null, "Esta es la dirección que ingresó del empleado #" + (i+1) + ": " + direcciones[i]);
            JOptionPane.showMessageDialog(null, "Esta es la área que ingresó del empleado #" + (i+1) + ": " + areas[i]);
            JOptionPane.showMessageDialog(null, "Este es el pago a la semana del empleado #" + (i+1) + ": " + pagoSemana[i]);
        }
    }
}
