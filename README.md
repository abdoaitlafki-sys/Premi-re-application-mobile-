# Premi-re-application-mobile-
import React, { useState } from 'react';
import {
  View,
  Text,
  StyleSheet,
  Pressable
} from 'react-native';

export default function App() {
  const [message, setMessage] = useState('Bonjour Campus !');

  return (
    <View style={styles.container}>

      {/* Etape 1 : Bonjour Campus */}
      <Text style={styles.title}>
        Bonjour Campus !
      </Text>

      {/* Etape 2 : Hello Campus */}
      <Text style={styles.subtitle}>
        Hello Campus !
      </Text>

      {/* Etape 3 : Affichage avec View et Text */}
      <View style={styles.box}>
        <Text style={styles.text}>
          Bienvenue dans React Native + Expo
        </Text>
      </View>

      {/* Etape 4 : Bouton Pressable */}
      <Text style={styles.message}>
        {message}
      </Text>

      <Pressable
        style={styles.button}
        onPress={() => {
          setMessage(
            message === 'Bonjour Campus !'
              ? 'Hello Campus !'
              : 'Bonjour Campus !'
          );
        }}
      >
        <Text style={styles.buttonText}>
          Changer le message
        </Text>
      </Pressable>

    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#F2F5F9',
    justifyContent: 'center',
    alignItems: 'center',
    padding: 20,
  },

  title: {
    fontSize: 28,
    fontWeight: 'bold',
    color: 'blue',
    marginBottom: 15,
  },

  subtitle: {
    fontSize: 24,
    color: 'green',
    marginBottom: 25,
  },

  box: {
    backgroundColor: 'white',
    padding: 20,
    borderRadius: 10,
    marginBottom: 25,
  },

  text: {
    fontSize: 18,
    color: 'black',
    textAlign: 'center',
  },

  message: {
    fontSize: 20,
    fontWeight: 'bold',
    marginBottom: 20,
  },

  button: {
    backgroundColor: 'blue',
    padding: 15,
    borderRadius: 8,
  },

  buttonText: {
    color: 'white',
    fontSize: 17,
    fontWeight: 'bold',
  },
});
