// tenho que colocar os modulos basica do funcionamento React Na
// 1º modulo de basico
import React, { useState } from 'react';
// 2º modulo, elementos visuais
import { View, Button, Image, Text, Pressable, StyleSheet } from 'react-native';
// função( MAIN, INDEX, )
function App() {
  // declarar variavel
  let img = 'Prestar *$#%%% !!!';
 
  // A  UMA QUESTÃO DE ESTADO DE MEMORIA AO REDINIZAR
  let [imgNome, setImgNome] = useState(' Prestar ');
  let [imagem, troca] = useState(require('./components/img/img02.jpg'));
 
  let imagens = [
        require('./components/img/img01.jpg'),
        require('./components/img/img02.jpg'),
        require('./components/img/img03.jpg'),
        require('./components/img/img04.jpg'),
 
      ]
 
    //função para trocar imagens
    let trocaImagem =( ) => {
          troca(imagens[3])
          i++;
    }
   // array com os nomes da imagens
   
   // colocar um contandor indice
 
  return (
    <View style={{ margin: 20 }}>
      <Image
        source={require('./components/img/img01.jpg')}
        style={estilo.img}
      />
      <Text>imagem {imgNome}</Text>
      <Button
        title="Ver"
        onPress={() => {
          setImgNome('Prestar *$#%%% !!!');
        }}
      />
 
      <Image source={imagem} style={estilo.img} />
 
      <Pressable
        style={estilo.bt}
        onPress={() => {
         // troca(require('./components/img/img01.jpg'));
         trocaImagem()
        }}>
        <Text> IMAGEM</Text>
      </Pressable>
    </View>
  );
}
// criar um  css incorporado
 
const estilo = StyleSheet.create({
  bt: {
    backgroundColor: '#ffaabb',
    color: '#000000',
    fontSize: 16,
    alignItems: 'center',
    marginTop: 10,
    padding: 5,
    borderRadius: 5,
  },
  img: {
    width: 200,
    height: 200,
    margin: 30,
  },
});
 
// Visibilidade da função
