package calculadora;

import java.awt.Color;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.*;

public class Principal {
	
    static double num1 = 0;
    static double num2 = 0;
    static double resultado;
    static String expressaoToda;
    static String sinal;
    static boolean resultadoExibido = false;
    
    public static void main(String[] args) {
        JFrame janela = new JFrame("Calculadora");
        StringBuilder textoCalcular = new StringBuilder();

        janela.setSize(400, 530);
        janela.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        janela.getContentPane().setBackground(Color.BLACK);

        JTextField calculando = new JTextField();
        calculando.setBounds(20, 60, 350, 100);
        janela.add(calculando);

        JButton ponto = new JButton(".");
        ponto.setBounds(janela.getWidth() - 89, 400, 60, 60);
        janela.add(ponto);

        ponto.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append(".");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoUm = new JButton("1");
        botaoUm.setBounds(janela.getWidth() - 89, 330, 60, 60);
        janela.add(botaoUm);

        botaoUm.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("1");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoDois = new JButton("2");
        botaoDois.setBounds(janela.getWidth() - 89, 260, 60, 60);
        janela.add(botaoDois);

        botaoDois.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("2");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoTres = new JButton("3");
        botaoTres.setBounds(janela.getWidth() - 89, 190, 60, 60);
        janela.add(botaoTres);

        botaoTres.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("3");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoZero = new JButton("0");
        botaoZero.setBounds(janela.getWidth() - 160, 400, 60, 60);
        janela.add(botaoZero);

        botaoZero.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("0");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoQuatro = new JButton("4");
        botaoQuatro.setBounds(janela.getWidth() - 160, 330, 60, 60);
        janela.add(botaoQuatro);

        botaoQuatro.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("4");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoCinco = new JButton("5");
        botaoCinco.setBounds(janela.getWidth() - 160, 260, 60, 60);
        janela.add(botaoCinco);

        botaoCinco.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("5");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoSeis = new JButton("6");
        botaoSeis.setBounds(janela.getWidth() - 160, 190, 60, 60);
        janela.add(botaoSeis);

        botaoSeis.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("6");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoSete = new JButton("7");
        botaoSete.setBounds(janela.getWidth() - 230, 330, 60, 60);
        janela.add(botaoSete);

        botaoSete.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("7");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoOito = new JButton("8");
        botaoOito.setBounds(janela.getWidth() - 230, 260, 60, 60);
        janela.add(botaoOito);

        botaoOito.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("8");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoNove = new JButton("9");
        botaoNove.setBounds(janela.getWidth() - 230, 190, 60, 60);
        janela.add(botaoNove);

        botaoNove.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (resultadoExibido) {
                    textoCalcular.setLength(0);
                    resultadoExibido = false;
                }
                textoCalcular.append("9");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoBack = new JButton("⌦");
        botaoBack.setBounds(janela.getWidth() - 300, 190, 60, 60);
        janela.add(botaoBack);

        botaoBack.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                if (textoCalcular.length() > 0) {
                    textoCalcular.deleteCharAt(textoCalcular.length() - 1);
                    calculando.setText(textoCalcular.toString());
                }
            }
        });

        JButton botaoAC = new JButton("AC");
        botaoAC.setBounds(janela.getWidth() - 300, 260, 60, 60);
        janela.add(botaoAC);

        botaoAC.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                textoCalcular.delete(0, textoCalcular.length());
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoMais = new JButton("+");
        botaoMais.setBounds(janela.getWidth() - 300, 330, 60, 60);
        janela.add(botaoMais);

        botaoMais.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                textoCalcular.append("+");
                calculando.setText(textoCalcular.toString());
            }
        });

        JButton botaoMenos = new JButton("-");
        botaoMenos.setBounds(janela.getWidth()-300,400,60,60);        
        janela.add(botaoMenos);
        
        botaoMenos.addActionListener(new ActionListener() {
        	public void actionPerformed(ActionEvent e) {
        		textoCalcular.append("-");
        		calculando.setText(textoCalcular.toString());
        	}
        });
        
        JButton botaoMulti = new JButton("*");
        botaoMulti.setBounds(janela.getWidth()-370,400,60,60);        
        janela.add(botaoMulti);
        
        botaoMulti.addActionListener(new ActionListener() {
        	public void actionPerformed(ActionEvent e) {
        		textoCalcular.append("*");
        		calculando.setText(textoCalcular.toString());
        	}
        });
        
        
        JButton botaoDivide = new JButton("/");
        botaoDivide.setBounds(janela.getWidth() - 230, 400, 60, 60);        
        janela.add(botaoDivide);
        
        botaoDivide.addActionListener(new ActionListener() {
        	public void actionPerformed(ActionEvent e) {
        		textoCalcular.append("/");
        		calculando.setText(textoCalcular.toString());
        	}
        });
        
        
        JButton botaoResultado = new JButton("=");
        botaoResultado.setBounds(janela.getWidth() -370,190,60,199);
        janela.add(botaoResultado);

        botaoResultado.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                expressaoToda = textoCalcular.toString();
                sinal = operadorMatematico(expressaoToda);
                
                if (sinal != null) {
                    int posicaoDoOperador = expressaoToda.indexOf(sinal);
                    try {
                        num1 = Double.parseDouble(expressaoToda.substring(0, posicaoDoOperador));
                        num2 = Double.parseDouble(expressaoToda.substring(posicaoDoOperador + 1));
                        
                        switch (sinal) {
                            case "+":
                                resultado = num1 + num2;
                                break;
                            case "-":
                                resultado = num1 - num2;
                                break;
                            case "*":
                                resultado = num1 * num2;
                                break;
                            case "/":
                                resultado = num1 / num2;
                                break;
                        }

                        textoCalcular.setLength(0);
                        textoCalcular.append(resultado);
                        calculando.setText(textoCalcular.toString());
                        resultadoExibido = true; 
                    } catch (NumberFormatException | StringIndexOutOfBoundsException ex) {
                        System.out.println("Erro ao calcular: " + ex.getMessage());
                        calculando.setText("Erro");
                    }
                }
            }
        });

        janela.setLayout(null);
        janela.setVisible(true);
    }

    public static String inverterTexto(String texto) {
        StringBuilder stringInvertida = new StringBuilder();
        for (int i = texto.length() - 1; i >= 0; i--) {
            stringInvertida.append(texto.charAt(i));
        }
        System.out.println("Inverteu: " + stringInvertida.toString());

        return stringInvertida.toString();
    }

    public static String operadorMatematico(String expressaoToda) {
        if(expressaoToda.contains("+")) {
            return "+";
        } else if(expressaoToda.contains("-")) {
            return "-";
        } else if(expressaoToda.contains("*")) {
            return "*";
        } else if(expressaoToda.contains("/")) {
            return "/";
        } else {
            return null;
        }
    }
}
