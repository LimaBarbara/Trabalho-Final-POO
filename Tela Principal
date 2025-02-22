package clinicanutricao;

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.util.Vector;

public class TelaPrincipal extends JFrame {
    JButton btnPaciente, btnNutricionista, btnAgendar, btnExibir;
    Vector<Paciente> pacientes = new Vector<>();
    Vector<Nutricionista> nutricionistas = new Vector<>();
    Vector<Consulta> consultas = new Vector<>();
    
    CadastroPaciente telaPaciente = new CadastroPaciente(this);
    CadastroNutricionista telaNutricionista = new CadastroNutricionista(this);
    AgendarConsulta telaConsulta = new AgendarConsulta(this);
    ExibirDados telaExibir = new ExibirDados(this);
    
    public TelaPrincipal() {
        setTitle("Clínica de Nutrição");
        setLayout(null);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        
        Handler handler = new Handler();
        
        btnPaciente = new JButton("Cadastrar Paciente");
        btnPaciente.setBounds(10, 10, 200, 30);
        btnPaciente.addActionListener(handler);
        add(btnPaciente);
        
        btnNutricionista = new JButton("Cadastrar Nutricionista");
        btnNutricionista.setBounds(10, 50, 200, 30);
        btnNutricionista.addActionListener(handler);
        add(btnNutricionista);
        
        btnAgendar = new JButton("Agendar Consulta");
        btnAgendar.setBounds(10, 90, 200, 30);
        btnAgendar.addActionListener(handler);
        add(btnAgendar);
        
        btnExibir = new JButton("Exibir Registros");
        btnExibir.setBounds(10, 130, 200, 30);
        btnExibir.addActionListener(handler);
        add(btnExibir);
        
        setBounds(100, 100, 300, 250);
        setVisible(true);
    }
    
    public void cadastrarPaciente(Paciente p) {
        pacientes.add(p);
    }
    
    public void cadastrarNutricionista(Nutricionista n) {
        nutricionistas.add(n);
    }
    
    public void cadastrarConsulta(Consulta c) {
        consultas.add(c);
    }
    
    class Handler implements ActionListener {
        public void actionPerformed(ActionEvent e) {
            if (e.getSource() == btnPaciente) {
                telaPaciente.setVisible(true);
            } else if (e.getSource() == btnNutricionista) {
                telaNutricionista.setVisible(true);
            } else if (e.getSource() == btnAgendar) {
                telaConsulta.setVisible(true);
            } else if (e.getSource() == btnExibir) {
                telaExibir.atualizarLista();
                telaExibir.setVisible(true);
            }
        }
    }
    
    public static void main(String[] args) {
        new TelaPrincipal();
    }
}
