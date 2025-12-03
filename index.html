import React, { useState, useEffect } from 'react';
import { HelpCircle, List, ArrowDownCircle, RefreshCw, Link as LinkIcon, CheckCircle } from 'lucide-react';

// Componente para renderizar blocos matemáticos (Display Math)
const MathJaxBlock = ({ latex }) => {
  useEffect(() => {
    if (window.MathJax && window.MathJax.typesetPromise) {
      window.MathJax.typesetPromise();
    }
  }, [latex]);

  return (
    <div 
      className="math-block overflow-x-auto p-4 bg-white rounded-lg border border-slate-200 my-4 text-slate-800 text-lg" 
      dangerouslySetInnerHTML={{ __html: `$$${latex}$$` }} 
    />
  );
};

// Componente para renderizar matemática inline
const InlineMath = ({ latex }) => {
  useEffect(() => {
    if (window.MathJax && window.MathJax.typesetPromise) {
      window.MathJax.typesetPromise();
    }
  }, [latex]);
  
  return <span dangerouslySetInnerHTML={{ __html: `$${latex}$` }} />;
};

export default function App() {
  const [activeStep, setActiveStep] = useState(0);

  // Efeito para carregar o MathJax dinamicamente
  useEffect(() => {
    if (!window.MathJax) {
      window.MathJax = {
        tex: {
          inlineMath: [['$', '$'], ['\\(', '\\)']],
          displayMath: [['$$', '$$'], ['\\[', '\\]']]
        },
        svg: {
          fontCache: 'global'
        }
      };
      
      const script = document.createElement('script');
      script.src = 'https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js';
      script.async = true;
      document.head.appendChild(script);
    } else if (window.MathJax.typesetPromise) {
      window.MathJax.typesetPromise();
    }
  }, []);

  // Efeito para re-renderizar matemática quando o passo muda
  useEffect(() => {
    if (window.MathJax && window.MathJax.typesetPromise) {
      // Pequeno delay para garantir que o DOM foi atualizado
      setTimeout(() => {
        window.MathJax.typesetPromise();
      }, 100);
    }
  }, [activeStep]);

  const steps = [
    {
      title: "O Problema",
      icon: <HelpCircle size={20} />,
      content: (
        <div className="space-y-4">
          <h2 className="text-2xl font-bold text-slate-800">Enunciado</h2>
          <p className="text-slate-600">
            Resolver a seguinte equação diferencial ordinária linear homogênea utilizando séries de potências em torno de <InlineMath latex="x_0 = 0" />:
          </p>
          <MathJaxBlock latex="y'' + x^2y' + xy = 0" />
          <p className="text-slate-600 font-semibold">Condições Iniciais:</p>
          <div className="flex gap-4">
            <div className="bg-blue-50 p-3 rounded-lg border border-blue-200 text-slate-800">
              <InlineMath latex="y(0) = 0" />
            </div>
            <div className="bg-blue-50 p-3 rounded-lg border border-blue-200 text-slate-800">
              <InlineMath latex="y'(0) = 1" />
            </div>
          </div>
        </div>
      )
    },
    {
      title: "1. Definição das Séries",
      icon: <List size={20} />,
      content: (
        <div className="space-y-4">
          <h2 className="text-2xl font-bold text-slate-800">Definindo a Série e Derivadas</h2>
          <p className="text-slate-600">
            Assumimos que a solução é uma série de potências. Precisamos calcular a primeira e a segunda derivada para substituir na equação original.
          </p>
          
          <div className="grid grid-cols-1 md:grid-cols-3 gap-4 mt-4">
            <div className="bg-white p-4 rounded shadow-sm border border-slate-200">
              <h3 className="font-bold text-slate-500 text-sm mb-2">FUNÇÃO ORIGINAL</h3>
              <div className="text-slate-800"><InlineMath latex="y(x) = \sum_{k=0}^{\infty} a_k x^k" /></div>
            </div>
            <div className="bg-white p-4 rounded shadow-sm border border-slate-200">
              <h3 className="font-bold text-slate-500 text-sm mb-2">PRIMEIRA DERIVADA</h3>
              <div className="text-slate-800"><InlineMath latex="y'(x) = \sum_{k=1}^{\infty} k a_k x^{k-1}" /></div>
            </div>
            <div className="bg-white p-4 rounded shadow-sm border border-slate-200">
              <h3 className="font-bold text-slate-500 text-sm mb-2">SEGUNDA DERIVADA</h3>
              <div className="text-slate-800"><InlineMath latex="y''(x) = \sum_{k=2}^{\infty} k(k-1) a_k x^{k-2}" /></div>
            </div>
          </div>
        </div>
      )
    },
    {
      title: "2. Substituição",
      icon: <ArrowDownCircle size={20} />,
      content: (
        <div className="space-y-4">
          <h2 className="text-2xl font-bold text-slate-800">Substituindo na EDO</h2>
          <p className="text-slate-600">
            Substituímos as expressões dos somatórios na equação <InlineMath latex="y'' + x^2y' + xy = 0" />.
          </p>
          <MathJaxBlock latex="\sum_{k=2}^{\infty} k(k-1) a_k x^{k-2} + x^2 \sum_{k=1}^{\infty} k a_k x^{k-1} + x \sum_{k=0}^{\infty} a_k x^k = 0" />
          
          <div className="bg-yellow-50 border-l-4 border-yellow-400 p-4 my-4">
            <p className="font-bold text-yellow-700">Atenção aos expoentes!</p>
            <p className="text-yellow-600 text-sm">
              Agora devemos multiplicar os termos de <InlineMath latex="x" /> que estão fora dos somatórios pelos termos de dentro. Lembre-se: <InlineMath latex="x^a \cdot x^b = x^{a+b}" />.
            </p>
          </div>

          <MathJaxBlock latex="\underbrace{\sum_{k=2}^{\infty} k(k-1) a_k x^{k-2}}_{(I)} + \underbrace{\sum_{k=1}^{\infty} k a_k x^{k+1}}_{(II)} + \underbrace{\sum_{k=0}^{\infty} a_k x^{k+1}}_{(III)} = 0" />
        </div>
      )
    },
    {
      title: "3. Ajuste de Índices",
      icon: <RefreshCw size={20} />,
      content: (
        <div className="space-y-4">
          <h2 className="text-2xl font-bold text-slate-800">Padronização dos Índices</h2>
          <p className="text-slate-600">
            Para somar tudo, todos os termos devem ter <InlineMath latex="x^k" />. Vamos fazer mudanças de variáveis nos índices.
          </p>

          <div className="grid gap-4">
            <div className="bg-white p-4 rounded border border-slate-200">
              <h3 className="font-bold text-indigo-600">Termo (I): Mudança k → k+2</h3>
              <p className="text-sm text-slate-500 mb-2">O expoente era k-2. Para virar k, aumentamos 2.</p>
              <div className="text-slate-800"><InlineMath latex="\sum_{k=0}^{\infty} (k+2)(k+1) a_{k+2} x^k" /></div>
            </div>

            <div className="bg-white p-4 rounded border border-slate-200">
              <h3 className="font-bold text-emerald-600">Termo (II): Mudança k → k-1</h3>
              <p className="text-sm text-slate-500 mb-2">O expoente era k+1. Para virar k, diminuímos 1.</p>
              <div className="text-slate-800"><InlineMath latex="\sum_{k=2}^{\infty} (k-1) a_{k-1} x^k" /></div>
            </div>

            <div className="bg-white p-4 rounded border border-slate-200">
              <h3 className="font-bold text-emerald-600">Termo (III): Mudança k → k-1</h3>
              <p className="text-sm text-slate-500 mb-2">O expoente era k+1. Para virar k, diminuímos 1.</p>
              <div className="text-slate-800"><InlineMath latex="\sum_{k=1}^{\infty} a_{k-1} x^k" /></div>
            </div>
          </div>
        </div>
      )
    },
    {
      title: "4. Relação de Recorrência",
      icon: <LinkIcon size={20} />,
      content: (
        <div className="space-y-4">
          <h2 className="text-2xl font-bold text-slate-800">Encontrando a Fórmula Geral</h2>
          <p className="text-slate-600">
            Igualamos os coeficientes a zero. Como os somatórios começam em índices diferentes (0, 2 e 1), separamos os primeiros termos (<InlineMath latex="k=0, k=1" />) do restante (<InlineMath latex="k \ge 2" />).
          </p>
          
          <div className="bg-slate-100 p-4 rounded text-slate-800">
            <h4 className="font-bold text-slate-700">Para k = 0:</h4>
            <InlineMath latex="(0+2)(0+1)a_2 = 0 \implies 2a_2 = 0 \implies \mathbf{a_2 = 0}" />
          </div>

          <div className="bg-slate-100 p-4 rounded text-slate-800">
            <h4 className="font-bold text-slate-700">Para k = 1:</h4>
            <InlineMath latex="6a_3 + a_0 = 0" />. Como <InlineMath latex="y(0)=a_0=0" />, então <InlineMath latex="\mathbf{a_3=0}" />.
          </div>

          <h3 className="font-bold text-slate-800 mt-4">Para k ≥ 2 (Recorrência):</h3>
          <MathJaxBlock latex="(k+2)(k+1)a_{k+2} + (k-1)a_{k-1} + a_{k-1} = 0" />
          <p className="text-slate-600">Simplificando:</p>
          <MathJaxBlock latex="a_{k+2} = -\frac{k}{(k+2)(k+1)} a_{k-1}" />
        </div>
      )
    },
    {
      title: "5. Solução Final",
      icon: <CheckCircle size={20} />,
      content: (
        <div className="space-y-4">
          <h2 className="text-2xl font-bold text-slate-800">Resultado</h2>
          <p className="text-slate-600">
            Usando <InlineMath latex="y'(0) = a_1 = 1" /> e a fórmula de recorrência:
          </p>

          <ul className="list-disc pl-5 space-y-2 text-slate-700">
            <li>Família <InlineMath latex="a_0" /> (0, 3, 6...): Todos Zero.</li>
            <li>Família <InlineMath latex="a_2" /> (2, 5, 8...): Todos Zero.</li>
            <li>Família <InlineMath latex="a_1" /> (1, 4, 7...): Sobrevivem!</li>
          </ul>

          <div className="overflow-x-auto text-slate-800">
            <table className="w-full text-left border-collapse mt-4">
              <thead>
                <tr className="border-b-2 border-slate-300">
                  <th className="py-2">k</th>
                  <th className="py-2">Cálculo</th>
                  <th className="py-2">Coeficiente</th>
                </tr>
              </thead>
              <tbody>
                <tr className="border-b border-slate-100">
                  <td className="py-2">2 (Gera <InlineMath latex="a_4"/>)</td>
                  <td className="py-2"><InlineMath latex="-\frac{2}{4 \cdot 3} \cdot 1"/></td>
                  <td className="py-2"><InlineMath latex="-1/6"/></td>
                </tr>
                <tr className="border-b border-slate-100">
                  <td className="py-2">5 (Gera <InlineMath latex="a_7"/>)</td>
                  <td className="py-2"><InlineMath latex="-\frac{5}{7 \cdot 6} \cdot (-1/6)"/></td>
                  <td className="py-2"><InlineMath latex="5/252"/></td>
                </tr>
              </tbody>
            </table>
          </div>

          <div className="bg-emerald-50 border border-emerald-200 p-6 rounded-lg mt-6">
            <h3 className="text-emerald-800 font-bold mb-2">Solução Geral:</h3>
            <MathJaxBlock latex="y(x) = x - \frac{1}{6}x^4 + \frac{5}{252}x^7 - \dots" />
            <p className="text-emerald-700 text-sm mt-2">Raio de convergência <InlineMath latex="R = \infty" /> (Converge para todo x).</p>
          </div>
        </div>
      )
    }
  ];

  return (
    <div className="flex flex-col md:flex-row h-screen bg-slate-50 font-sans">
      {/* Sidebar de Navegação */}
      <div className="w-full md:w-64 bg-slate-900 text-white p-6 flex flex-col shrink-0 overflow-y-auto">
        <div className="mb-8">
          <h1 className="text-xl font-bold tracking-tight">Séries de Potência</h1>
          <p className="text-slate-400 text-sm mt-1">Exercício 11 Resolvido</p>
        </div>
        
        <nav className="space-y-2 flex-1">
          {steps.map((step, index) => (
            <button
              key={index}
              onClick={() => setActiveStep(index)}
              className={`w-full text-left px-4 py-3 rounded-lg transition-colors flex items-center gap-3 ${
                activeStep === index 
                ? 'bg-blue-600 text-white font-medium shadow-lg' 
                : 'text-slate-300 hover:bg-slate-800'
              }`}
            >
              <span className="shrink-0">
                {step.icon}
              </span>
              <span className="text-sm font-medium">
                {step.title}
              </span>
            </button>
          ))}
        </nav>
        
        <div className="mt-8 pt-6 border-t border-slate-800 text-xs text-slate-500">
          Baseado na resolução enviada.
        </div>
      </div>

      {/* Área de Conteúdo */}
      <main className="flex-1 p-6 md:p-12 overflow-y-auto">
        <div className="max-w-3xl mx-auto">
          {/* Header Mobile */}
          <div className="md:hidden mb-6 pb-6 border-b border-slate-200">
            <h2 className="text-slate-500 text-sm uppercase tracking-wide font-semibold">Passo Atual</h2>
            <h1 className="text-2xl font-bold text-slate-900">{steps[activeStep].title}</h1>
          </div>

          {/* Conteúdo do Card */}
          <div className="bg-white rounded-xl shadow-xl border border-slate-100 overflow-hidden min-h-[500px]">
            <div className="p-8">
              {steps[activeStep].content}
            </div>
            
            {/* Footer de Navegação Interna */}
            <div className="bg-slate-50 px-8 py-4 border-t border-slate-100 flex justify-between items-center">
              <button 
                onClick={() => setActiveStep(Math.max(0, activeStep - 1))}
                disabled={activeStep === 0}
                className={`px-4 py-2 rounded font-medium transition-colors ${activeStep === 0 ? 'text-slate-300 cursor-not-allowed' : 'text-slate-600 hover:bg-slate-200'}`}
              >
                &larr; Anterior
              </button>
              
              <span className="text-sm text-slate-400 font-medium">
                Passo {activeStep + 1} de {steps.length}
              </span>

              <button 
                onClick={() => setActiveStep(Math.min(steps.length - 1, activeStep + 1))}
                disabled={activeStep === steps.length - 1}
                className={`px-4 py-2 rounded font-medium transition-colors ${activeStep === steps.length - 1 ? 'text-slate-300 cursor-not-allowed' : 'bg-blue-600 text-white hover:bg-blue-700 shadow-md'}`}
              >
                Próximo &rarr;
              </button>
            </div>
          </div>
        </div>
      </main>
    </div>
  );
}
