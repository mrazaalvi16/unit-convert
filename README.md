import streamlit as st
def convert_units(value :float, unit_from: str, unit_to:str):
    # print("value>>>", value)
    # print("unit_from>>>", unit_from)
    # print("unit_to>>>", unit_to)

    if unit_from == "kilometers" and unit_to == "meters":
        return value * 1000
    elif unit_from == "meters" and unit_to == "kilometers":
        return value * 0.001
    elif unit_from == "kilograms" and unit_to == "grams":
        return value * 1000
    elif unit_from == "grams" and unit_to == "kilograms":
        return value * 0.001
    else:
        return "conversion is not supported"
    
# result1 = convert_units(1.5, "kilometers", "meters")
# print("The value in meter is:", result1)
# result2 = convert_units(3, "grams", "kilograms")
# print("The value in meter is:", result2)    
_
def main():
    st.title("unit converter")
    st.write("welcome to unit converter!")
    value = st.mumber_input("Enter the value you want to convert:", min_value=0.0)
    unit_from = st.text_input("Enter the value you want to convert from (e.g. meter,kilometers, grams,kilograms)")
    unit_to = st.text_input("Enter the value you want from conversion (e.g. meter,kilometers, grams,kilograms)")

    if st.button("Convert"):
        result = convert_units(value, unit_from, unit_to)
        st.write("Converted value is:", result)
    
    # print("value", value)
    # print("unit_from", unit_from)
    # print("unit_to", unit_to)
    # result = convert_units(value, unit_from,unit_to)
    # print("Converted value is:", result)

main()# unit-convert
